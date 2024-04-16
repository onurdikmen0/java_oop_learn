__Bu bölümde neler var?__
- Soyutlama (Abstraction)
- Abstract Class(Soyut Sınıf)



## Soyutlama (Abstraction)
Soyutlama nesnenin sadece önemli olan kısımlarının görünmesini sağlar. Önemsiz, ayrıntı kısımların görünmesini engeller.
Soyutlama sadeleşme sağlar ve bilgininde gizlenmesini sağlar.
Soyutlama için bir örnek: Kahve makinasını bir nesne olarak düşünelim kullanıcılar sadece kahve yapma işlevini düşünür, düğmeye basarak istenilen özelliklerde kahve yapma talimatı veririz, içerideki detaylarla uğraşmaz.

## Abstract Class(Soyut Sınıf)
- Kendisinden nesne türetilemeyen sınıflardır.
- Soyut sınıflar diğer sınıflardan kalıtım almak ve ortak özellikleri paylaşmak için kullanılırlar.
- Soyut sınıflar soyut yöntem(metod)lar içerebilir.
- Soyut sınıflar ortak özellikleri paylaşan sınıfları bir araya getirir.
- Soyut sınıflar programların daha küçük ve daha yönetilebilir birimlere bölünmesini sağlar.
- Soyut yöntemler bir gövdeye(imzalı kodsuz metod) sahip olmayan yöntemlerdir.
- Soyut yöntemler soyut sınıftan türetilen sınıflarda tanımlanmalıdır.


![alt text](image\image7.png){class="resim"} 
Yukarıda Shape(şekil) ana sınıfını ve onun alt sınıfalrı olan Rectangle(dikdörtgen), Triangle(üçgen), Rectangle sınıfının alt sınıfı olarakta Square(kare) alt sınıfı şeklinde bir model tasarladık. Bu modelde Shape sınıfından bir nesne türetmemiz mantıksız olacağından bu sınıfı abstract class olarak güncelleyebiliriz. Shape sınıfımız bizim için bir şablon görevi görecek. 

```java
  public abstract class Shape{

  }
```
Shape sınıfına bir de draw() adında alt sınıflarda kullanmak için abstract method tanımladık. 
Bu metod:

```java
  public abstract void draw();
```

görüldüğü üzere abstract anahtar kelimesi ile abstract metod olduğu belirtilir. Abstarct metod olduğu içinde metodun sadece imzası vardır, body(gözde) kısmı yoktur. Metodun gövdesi her alt sınıfta yeniden (kendine özgü) yazılması zorunludur.
```java
    @Override
    public void draw(){
      System.out.println("Dikdörtgen çizildi değerleri x : "+ getX() + " y : "+ getY());
    }
```


