---
youtube: https://youtu.be/UkfEBZ6Iw7w
aparat: https://aparat.com/v/aoz04th
date: 2025-07-21
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - برنامه_نویسی
  - سی_شارپ
  - class
  - OOP
title: آموزش برنامه نویسی با سی شارپ C# - قسمت 10 – کلاس (Class)
summary: توی این قسمت میخوایم با یه مفهوم خیلی خیلی مهم دیگه به اسم class آشنا بشیم.
duration: 831
---
# کلاس (Class) چیه؟
# ساخت کلاس `Player`
```cs
class Player
{
    bool isDead = false;
    float health = 100f;
    int hits = 0;
    void PrintPlayerStats()
    {
        Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
    }
    float TakeDamage(float amount = 1f)
	{
	    if (isDead)
	    {
	        return health;
	    }
	    health -= amount;
	    hits++;
	    if (health <= 0f)
	    {
	        isDead = true;
	        health = 0f;
	    }
	    PrintPlayerStats();
	    return health;
	}
}
```

# ساخت یک Player جدید

```cs
Player ali = new Player();
ali.TakeDamage();
```

```cs
Player ali = new Player();
ali.TakeDamage();
Player reza = new Player();
reza.TakeDamage(3);
```

# فیلد coin
```cs
Player ali = new Player();
ali.TakeDamage();
Player reza = new Player();
reza.TakeDamage(3);


class Player
{
    bool isDead = false;
    float health = 100f;
    int hits = 0;
    int coins = 0;
    void PrintPlayerStats()
    {
        Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
        Console.WriteLine($"Coins: {coins}");
    }
    float TakeDamage(float amount = 1f)
	{
	    if (isDead)
	    {
	        return health;
	    }
	    health -= amount;
	    hits++;
	    if (health <= 0f)
	    {
	        isDead = true;
	        health = 0f;
	    }
	    PrintPlayerStats();
	    return health;
	}
}

```

# اضافه کردن `PlayerName`
```cs
Player ali = new Player();
ali.playerName = "Ali";
ali.TakeDamage();

Player reza = new Player();
reza.playerName = "Reza";
reza.TakeDamage(3);
class Player
{
    bool isDead = false;
    float health = 100f;
    int hits = 0;
    int coins = 0;
    public string playerName = "No Name";
    void PrintPlayerStats()
    {
        Console.WriteLine($"Name: {playerName}");
        Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
        Console.WriteLine($"Coins: {coins}");
    }
    public float TakeDamage(float amount = 1f)
    {
        if (isDead)
        {
            return health;
        }
        health -= amount;
        hits++;
        if (health <= 0f)
        {
            isDead = true;
            health = 0f;
        }
        PrintPlayerStats();
        return health;
    }
}

```

# Field, Method, Instance, Object, Initialization

# استفاده از تایپمون به عنوان یک فیلد

```cs
Car honda = new Car();
honda.Drive();

CarBooster booster = new CarBooster();
booster.car = honda;
booster.BoostSpeed(80f);

class Car
{
    public float speed = 99f;
    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}
class CarBooster
{
    public Car car;
    public void BoostSpeed(float speed)
    {
        Console.WriteLine("Boosting Speed ...");
        Console.WriteLine($"New Speed: {car.speed + speed}");
    }
}
```

# استفاده از تایپمون توی return


```cs
CarFactory factory = new CarFactory();
Car honda = factory.Create(120f);
honda.Drive();

Car bmw = factory.Create(160f);
bmw.Drive();

class Car
{
    public float speed = 99f;
    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}

class CarFactory
{
    public Car Create(float speed)
    {
        Car car = new Car();
        car.speed = speed;
        Console.WriteLine($"Car Created. Speed: {car.speed}kmph!");
        return car;
    }
}
```

# پاس دادن تایپمون به عنوان پارامتر
```cs
CarFactory factory = new CarFactory();
Car honda = factory.Create(120f);
honda.Drive();

Car bmw = factory.Create(160f);
bmw.Drive();

Parking parking = new Parking();
parking.Park(honda);
parking.Park(bmw);
class Car
{
    public float speed = 99f;
    public void Drive()
    {
        Console.WriteLine($"Driving {speed}kmph...");
    }
}

class CarFactory
{
    public Car Create(float speed)
    {
        Car car = new Car();
        car.speed = speed;
        Console.WriteLine($"Car Created. Speed: {car.speed}kmph!");
        return car;
    }
}

class Parking
{
    public void Park(Car car)
    {
        Console.WriteLine($"Parked. Car Speed: {car.speed}kpmh.");
    }
}
```

# استفاده از سینتکس جدید `new` 
```cs
Car honda = new();
honda.Drive();

Car bmw = new();
bmw.Drive();
```

# جدا کردن فایل های کلاس
