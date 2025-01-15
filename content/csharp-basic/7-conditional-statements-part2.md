---
youtube: https://youtube.com/watch?v=51Z5ZinEFwY
aparat: https://www.aparat.com/v/doz8f4r
date: 2024-11-08
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - برنامه_نویسی
  - سی_شارپ
  - دستورات_شرطی
  - مقدماتی
title: آموزش برنامه نویسی با سی شارپ C# قسمت 7 – دستورات شرطی - بخش 2 از 2
summary: دستورات شرطی - بخش دوم
duration: 668
---
```cs
float health = 100f;

if (health == 100f)
{
    Console.WriteLine("Full");
} else
{
    Console.WriteLine("Not Full");
}
```


```cs
float health = 30f;

if (health > 70)
{
    Console.WriteLine("Health: FULL");
}
else if (health <= 70 && health > 50)
{
    Console.WriteLine("Health: NORMAL");
}
else if (health <= 50 && health > 10)
{
    Console.WriteLine("Health: LOW");
}
else
{
    Console.WriteLine("Health: DANGER");
}
```

```cs
string playerState = "RUNNING";

if (playerState == "IDLE")
{
    Console.WriteLine("Player is IDLE");
}
else if (playerState == "WALKING")
{
    Console.WriteLine("Player is WALKING");
}
else if (playerState == "RUNNING")
{
    Console.WriteLine("Player is RUNNING");
}
else if (playerState == "JUMPING")
{
    Console.WriteLine("Player is JUMPING");
}
else
{
    Console.WriteLine("Player is DEAD");
}

string playerState = "RUNNING";

switch (playerState)
{
    case "IDLE":
        Console.WriteLine("Player is IDLE");
        break;
    case "WALKING":
        Console.WriteLine("Player is WALKING");
        break;
    case "RUNNING":
        Console.WriteLine("Player is RUNNING");
        break;
    case "JUMPING":
        Console.WriteLine("Player is JUMPING");
        break;
    default:
        Console.WriteLine("Player is DEAD");
        break;
}
```



```cs
bool thisIsTrue = true;

if (thisIsTrue == true)
{
    Console.WriteLine("Inside IF");
}

if (thisIsTrue)
{
    Console.WriteLine("Inside IF");
}


```


```cs
bool condition = true && 3 == 3 && 6 == 6;

if (condition)
{
    Console.WriteLine("Inside IF");
}
```

```cs
if (true || 10 < 3 || false == true)
{
    Console.WriteLine("Inside IF");
}
else
{
    Console.WriteLine("Outside IF");
}

```

```cs
if (true || 10 < 3 || false == true)
{
    Console.WriteLine("Inside IF");
}
else
{
    Console.WriteLine("Outside IF");
}
```

```cs
bool condition = ((9 == 9) && !false) && (true && true);

if (condition)
{
    Console.WriteLine("Inside IF");
}
```



```cs
float health = 100f;

switch (name)
{
    case "name":
        Console.WriteLine("Greater Than");
        break;
    default:
        Console.WriteLine("nothing");
        break;
}
```