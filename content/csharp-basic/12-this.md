---
youtube: https://youtu.be/UKNdD-PlS2M
aparat: https://aparat.com/v/gxm1j46
date: 2025-07-24
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - سی_شارپ
  - برنامه_نویسی
  - مفاهیم
title: آموزش برنامه نویسی با سی شارپ C# - قسمت 12 – this
summary: توی این بخش میخوایم در مورد keyword یا کلمه کلیدی this صحبت کنیم.
duration: 323
---
# آشنایی با `this`
```cs
Car honda = new(120f);
honda.Drive();

Car bmw = new(160f);
bmw.Drive();

class Car
{
    public float speed = 99f;
    public Car(float speed)
    {
        this.speed = speed;
    }
    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}
```

# استفاده از `this` در `return`

```cs
public Car IncreaseSpeed(float speed) { 
    this.speed += speed;
    return this;
}
```

```cs
Car honda = new(120f);
honda.Drive();

honda.IncreaseSpeed(10);
honda.Drive();
```

```cs
Car honda = new(120f);
honda.Drive();

honda.IncreaseSpeed(10).Drive();
honda.IncreaseSpeed(100).Drive();
honda.IncreaseSpeed(10).Drive();
```


```cs
Car honda = new(120f);
honda.IncreaseSpeed(10).IncreaseSpeed(20).IncreaseSpeed(30).Drive();
```

```cs
Car honda = new(120f);
honda.IncreaseSpeed(10);
honda.IncreaseSpeed(20);
honda.IncreaseSpeed(30);
honda.Drive();
```

# استفاده از `this` به عنوان ورودی متد ها

```cs
class Car
{
    public float speed = 99f;
    Parking parking = new();

    public Car(float intialSpeed)
    {
        this.speed = intialSpeed;
    }

    public void ParkMe()
    {
        parking.Park(this);
    }
}
```

# بی معنی بودن استفاده از `this` یه سری از جاها

```cs
public Car(float intialSpeed)
{
    this.speed = intialSpeed;
}
```

```cs
public float GetSpeed()
{
    return this.speed;
}
```