# Final Test 1
## Задача:
### Написать программу, которая из имеющегося массива строк формирует массив из строк, длина которых меньше либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решение не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.


```
Примеры:
[“Hello”, “2”, “world”, “:-)”] → [“2”, “:-)”]
[“1234”, “1567”, “-2”, “computer science”] → [“-2”]
[“Russia”, “Denmark”, “Kazan”] → []
```
## Описание алгоритма решения:
#### Сначала объявляется два массива одинаковой длины:
```C#
﻿﻿string[] array1 = new string[5] {"344", "1567", "Russia", "-2", "13"};
string[] array2 = new string[array1.Length];
```
### Далее добовляем метод, в котором цикл ограничен длиной. Условие проверяет длину элемента масива *array1* , если длина эоемента меньше или равна 3 то заноситься в масив  *array2*:
```csharp
void SecondArray(string[] array1, string[] array2)
{
    int count = 0;
    for (int i = 0; i < array1.Length; i++)
    {
    if(array1[i].Length <= 3)
        {
        array2[count] = array1[i];
        count++;
        }
    }
}
```
### Добовляем метод для вывода результата:

```csharp
void PrintArray(string[] array)
{
    for (int i = 0; i < array.Length; i++)
    {
        Console.Write($"{array[i]} ");
    }
    Console.WriteLine();
}
```
### И в конце выводим результат:
```csharp
SecondArray(array1, array2);
PrintArray(array2);
```
