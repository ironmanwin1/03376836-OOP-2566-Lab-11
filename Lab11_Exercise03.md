# Lab 11 Exercise 3

## Runtime polymorphism

1.สร้าง console application project

```cmd
dotnet new console --name Lab11_Ex03
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
var animalA = new Dog();
var animalB = new Fish();
var animalC = new Bird();

animalA.Move();
animalB.Move();
animalC.Move();

class Animal
{
   public virtual void Move()
   {
    System.Console.WriteLine("Move successfully.");
   } 
}

class Dog:Animal
{
    public override void Move()
    {
        System.Console.WriteLine($"{this.GetType()}: Running on the ground.");
        base.Move();
    }
}
class Fish: Animal
{
    public override void Move()
    {
        System.Console.WriteLine($"{this.GetType()}: Swimming in the water.");
        base.Move();
    }
}

class Bird: Animal
{
    public override void Move()
    {
        System.Console.WriteLine($"{this.GetType()}: Flying in the air.");
        base.Move();
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab11_Ex03
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab11_Ex03
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

7.อธิบายสิ่งที่พบในการทดลอง
