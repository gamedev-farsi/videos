---
youtube: https://youtube.com/watch?v=baf6wVztg10
aparat: https://www.aparat.com/v/qvx43p4
date: 2024-11-01
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - سی_شارپ
  - برنامه_نویسی
  - مقدماتی
title: آموزش برنامه نویسی با سی شارپ C# - قسمت 5 – تبدیل دیتا تایپ ها
summary: تبدیل دیتا تایپ ها به هم
duration: 550
---
```cs
float health = 33.33f;
Console.WriteLine($"Health: {health}");
```


```cs
float health = 33.33f;
int healthAsInt = health;
```


```cs
float health = 33.33f;
int healthAsInt = (int)health;
Console.WriteLine($"Float ({health}) -> Int ({healthAsInt})");
```


```cs
int damage = 10;
float damageAsFloat = damage;
Console.WriteLine($"int ({damage}) -> Int ({damageAsFloat})");
```

```cs
int myNumber = int.MaxValue;
long myNumberAsLong = myNumber;
Console.WriteLine($"Int ({myNumber}) -> Long ({myNumberAsLong})");
```

```cs
long aGrowingNumber = 999;
int aGrowingNumberAsInteger = aGrowingNumber;
```

```cs
long aGrowingNumber = 999;
int aGrowingNumberAsInteger = (int)aGrowingNumber;
Console.WriteLine($"Long ({aGrowingNumber}) -> Int ({aGrowingNumberAsInteger})");
```

```cs
long aBigNumber = 9999999999999999;
int aBigNumberAsInteger = (int)aBigNumber;
Console.WriteLine($"Long ({aGrowingNumber}) -> Int ({aGrowingNumberAsInteger})");
```

```cs
long aBigNumber = 9999999999999999;
int aBigNumberAsInteger = (int)aBigNumber;
Console.WriteLine($"Long ({aBigNumber}) -> Int ({aBigNumberAsInteger})");
```


| امتیاز        | تعداد ستاره |
| ------------- | ----------- |
| بین 0 تا 29   | صفر ستاره   |
| بین 30 تا 59  | 1 ستاره ⭐   |
| بین 60 تا 89  | 2 ستاره ⭐⭐  |
| بین 90 تا 100 | 3 ستاره ⭐⭐⭐ |

```cs
float health = 100f;
int stars = health / 30;
```


```cs
float health = 13f;
int stars = (int)health / 30;

Console.WriteLine($"Float ({health}) -> Int ({stars})");

```


```cs
int nine = 9;
int two = 2;

float nineDividedByTwo = (float)nine / two;
Console.WriteLine(nineDividedByTwo);
```

```cs
float points = 396.3f;
int level = points / 100f;

```

```cs
float points = 396.3f;
int level = (int)(points / 100f);
Console.WriteLine($"points ({points}) -> level ({level})");
```

```cs
int three = (int)"3";
```


```cs
int three = Convert.ToInt32("3");
Console.WriteLine($"String (3) -> Int ({three})");
```

```cs
int stars = 3;
double radius = 9.36;
bool learning = true;

Console.WriteLine($"Int ({stars}) -> String ({Convert.ToString(stars)})");
Console.WriteLine($"Int ({stars}) -> Double ({Convert.ToDouble(stars)})");
Console.WriteLine($"Double ({radius}) -> Int ({Convert.ToInt32(radius)})");
Console.WriteLine($"Bool ({learning}) -> String ({Convert.ToString(learning)})");
```

# لینک های مرتبط
- https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/types/casting-and-type-conversions
- 
