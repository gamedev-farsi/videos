---
youtube: https://youtube.com/watch?v=znf8_PHJc1o
aparat: https://www.aparat.com/v/ezjws53
date: 2025-01-07
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - سی_شارپ
  - برنامه_نویسی
  - فانکشن
  - مقدماتی
title: آموزش برنامه نویسی با سی شارپ C# - قسمت 8 – فانکشِن ها (Functions)
summary: توی این قسمت میخوایم با فانکشِن (Function) آشنا بشیم
duration: 659
---
# What is function?

```csharp
datatype Name(Parameters ...) 
{
	// process
	// return
	return output;
}
```

```cs
bool isDead = false;
float health = 100f;
int hits = 0;

float TakeDamage(float amount = 33f)
{
    hits++;
    health -= amount;
    if (health <= 0)
    {
        health = 0;
        isDead = true;
    }
    PrintPlayerStats();
    return health;
}
void PrintPlayerStats()
{
    Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
}

PrintPlayerStats();
TakeDamage();
TakeDamage(9);
TakeDamage(3);
TakeDamage();
TakeDamage();


```

```cs
float Divide(int first, int second)
{
    return (float)first / second;
}

Console.WriteLine(Divide(9, 3));
Console.WriteLine(Divide(3, 9));
```

```csharp
void PrintPlayerStats()
{
    Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
}
```

```cs
float Divide(int first, int second)
{
    return (float)first / second;
}

Console.WriteLine(Divide(9, 3));
Console.WriteLine(Divide(3, 9));

```


```cs
void Shoot()
{
    if (isDead)
    {
        return;
    }
    // Shoot logic
}

void Shoot()
{
    if (!isDead)
    {
        // Shoot logic
    }
}
```


```cs
int Add(int a, int b)
{
    int result = a + b;
    return result;
}

int threePlusSix = Add(3, 6);
```

```cs
void PrintPlayerStats()
{
    Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
}

PrintPlayerStats(); // Output: Health: 92.8 | Dead: False | Hits: 2.
```

```csharp
void PrintHello(string playerName)
{
    Console.WriteLine($"Hello my friend, {playerName}!");
}

PrintHello("GameDevFarsi"); // Output: Hello my friend, GameDevFarsi!
```


```cs
bool isDead = false;
void Shoot()
{
    if (isDead)
    {
        Console.WriteLine("Can't shoot, player is dead");
        return;
    }
    Console.WriteLine("here");
    
    // Shoot logic
}
Shoot();
```


```cs
float TakeDamage(float amount)
{
    hits++;
    health -= amount;
    if (health <= 0)
    {
        health = 0;
        isDead = true;
    }
    PrintPlayerStats();
    return health;
}
void PrintPlayerStats()
{
    Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
}

TakeDamage(enemyDamage);
TakeDamage(enemyDamage);
TakeDamage(enemyDamage * 30);
```


