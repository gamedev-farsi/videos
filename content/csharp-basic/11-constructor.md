---
youtube: https://youtu.be/14831jzqKKg
aparat: https://aparat.com/v/kbi39h1
date: 2025-07-24
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - برنامه_نویسی
  - مفاهیم
  - سی_شارپ
title: آموزش برنامه نویسی با سی شارپ C# - قسمت 11 – Constructor
summary: توی این قسمت میخوایم با constructor ها آشنا شیم.
duration: 528
---
# Constructor چیه ؟


```cs
Car honda = new();
honda.speed = 120f;
honda.Drive();

Car bmw = new();
bmw.speed = 160f;
bmw.Drive();

class Car
{
    public float speed = 99f;
    public Car()
    {
        Console.WriteLine("Object Created");
    }
    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}
```

```cs
Car honda = new(120f);
honda.Drive();

Car bmw = new(160f);
bmw.Drive();

class Car
{
    public float speed = 99f;
    public Car(float intialSpeed)
    {
        speed = intialSpeed;
    }
    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}
```

# استفاده از Constructor برای Logic

```cs

class Car
{
    public float speed = 99f;
    public Car(float intialSpeed)
    {
        speed = intialSpeed;
        CheckFuel();
        CheckEngine();
        StartEngine();
        Drive();
    }

    void CheckFuel()
    {
        Console.WriteLine($"Fuel Ok!");
    }
    void CheckEngine()
    {
        Console.WriteLine($"Engine Checked, Ok!");
    }
    void StartEngine()
    {
        Console.WriteLine($"Engine Started");
    }
    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}
```

# Object Initializer

```cs
Car honda = new();
honda.speed = 99f;
honda.fuel = 60f;
```

```cs
Car honda = new()
{
    speed = 99f,
    fuel = 60f
};
```
# Primary Constructors
```cs
class Car(float intialSpeed)
{
    public float speed = intialSpeed;

    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}
```

# لینک های مرتبط
- https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/object-and-collection-initializers#object-initializers
- https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/tutorials/primary-constructors