---
youtube: https://youtube.com/watch?v=qxZJk8IvCXo
aparat: https://www.aparat.com/v/kid026k
date: 2024-11-08
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - سی_شارپ
  - برنامه_نویسی
  - مقدماتی
  - دستورات_شرطی
title: آموزش برنامه نویسی با سی شارپ C# قسمت 6 – دستورات شرطی - بخش 1 از 2
summary: دستورات شرطی - بخش اول
duration: 482
---
```cs
bool isDead = false;
float health = 100f;
int hits = 0;
float enemyDamage = 3.6f;
```

```cs
hits = hits + 1;
health = health - enemyDamage;
Console.WriteLine(health);
```

```cs
health += enemyDamage; // health = health + enemyDamage;
health *= enemyDamage; // health = health * enemyDamage;
health /= enemyDamage; // health = health / enemyDamage;
```

```cs
Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");

// take damage
hits = hits + 1; // hits++;
health = health - enemyDamage; // health -= enemyDamage;

Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
```

```cs
Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");

// take damage
hits = hits + 1; // hits++;
health = health - enemyDamage;

Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");

// take damage
hits = hits + 1; // hits++;
health = health - enemyDamage;

Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");

// take damage
hits = hits + 1; // hits++;
health = health - 90;

Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");
```


```
if (condition)
{
	// do something	
}
```


```cs
int hits = 1;

if (hits == 0)
{
    Console.WriteLine("No Hit");
    
}
```


```cs
int hits = 1;

if (hits >= 0)
{
    Console.WriteLine("Greater Than Or Equal");
}
if (hits <= 0)
{
    Console.WriteLine("Less Than Or Equal");
}

```


```cs
if (health <= 0)
{
    health = 0;
	isDead = true;
}
```

```cs
bool isDead = false;
float health = 100f;
int hits = 0;
float enemyDamage = 3.6f;

// Take Damage
hits++; 
health -= enemyDamage;
if (health <= 0)
{
    health = 0;
    isDead = true;
}
Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");

// Take Damage
hits++;
health -= enemyDamage;
if (health <= 0)
{
    health = 0;
    isDead = true;
}
Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");

// Take Damage
hits++;
health -= enemyDamage * 30;
if (health <= 0)
{
    health = 0;
    isDead = true;
}
Console.WriteLine($"Health: {health} | Dead: {isDead} | Hits: {hits}.");


```



