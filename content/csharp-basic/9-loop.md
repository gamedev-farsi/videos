---
youtube: https://youtu.be/Mo9h1y_0980
aparat: https://aparat.com/v/mtk0j61
date: 2025-07-21
draft: false
category: "سری آموزش های برنامه نویسی با سی شارپ #C (مقدماتی)"
author: علی
tags:
  - سی_شارپ
  - برنامه_نویسی
  - مقدماتی
  - loop
title: آموزش برنامه نویسی با سی شارپ C# - قسمت 9 – حَلقه (Loop)
summary: توی این قسمت میخوایم با یک مفهوم مهم دیگه توی برنامه نویسی به اسم حلقه یا loop آشنا بشیم.
duration: 944
---
# لوپ یا حلقه چیه؟
# حلقه `While`
```cs
while (condition)
{
    // do something ...
}
```

```cs
int totalHits = 0;
while (totalHits < 100)
{
    TakeDamage();
    totalHits++;
}
```

# حلقه `do while`
```cs
int totalHits = 0;
do {
	TakeDamage();
	totalHits++;
}
while(totalHits < 100);
```
# حلقه `for`
```cs
for (int totalHits = 0; totalHits < 100; totalHits++)
{
    TakeDamage();
}
```

# کیورد `break`
```cs
while (true)
{
    TakeDamage();
    if (health < 10)
    {
        break;
    }
}
```
# کیورد `continue`

```cs
int totalLevels = 10;
int magicLevel1 = 3;
int magicLevel2 = 6;
void CreateLevel(int level)
{
    Console.WriteLine($"Level {level} created!");
}

for (int levelNumber = 1; levelNumber <= totalLevels; levelNumber++)
{
    if (levelNumber == magicLevel1 || levelNumber == magicLevel2)
    {
        continue;
    }
    CreateLevel(levelNumber);
}
```
# حلقه بی نهایت (Infinite Loop) با `for`

```cs
for (; ; )
{
    Console.WriteLine("Boom!");
    TakeDamage();
    if (isDead)
    {
        break;
    }
}
Console.WriteLine("Loop finished");
```

# حلقه های تو در تو - Nested Loops
```cs
int rows = 6;
int columns = 6;

for (int row = 0; row < rows; row++)
{
    for (int column = 0; column < columns; column++)
    {
        Console.Write($" # ");
    }
    Console.WriteLine();
}
```

```cs
int rows = 6;
int columns = 6;

for (int row = 0; row < rows; row++)
{
    for (int column = 0; column < columns; column++)
    {
        Console.Write($" ({column}, {row}) ");
    }
    Console.WriteLine();
}
```

```cs
int rows = 6;
int columns = 6;

for (int row = 0; row < rows; row++)
{
    for (int column = 0; column < columns; column++)
    {
        if (row == 3 && column == 1 )
        {
            Console.Write($" ###### ");
            continue;
        }
        Console.Write($" ({column}, {row}) ");
    }
    Console.WriteLine();
}
```

```cs
int rows = 6;
int columns = 6;

for (int i = 0; i < rows; i++)
{
    for (int j = 0; j < columns; j++)
    {
        Console.Write($" ({j}, {i}) ");
    }
    Console.WriteLine();
}
```