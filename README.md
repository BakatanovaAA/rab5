#   Работа 5
## Вариант 1
## Код
```c
#define _CRT_SECURE_NO_DEPRECATE
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#define M_PI 3.14159265358979323846
int main()
{
    task1();
    task23();

    return 0;
}

int task1()
{
    double gr, res;

    setlocale(LC_ALL, "RUS");

    puts("Введите угол в градусах");
    scanf("%lf", &gr);

    res = sin(gr * M_PI / 180);

    printf("sin(%.0f град) = %.6f\n", gr, res);

    system("pause");
    return 0;
}

int task23()
{
    double x, y, a, b;
    double c = 0.4;
    int A, B, C;
    int usl1, usl2;

    setlocale(LC_ALL, "RUS");

    puts("Введите x");
    scanf("%lf", &x);

    a = log10(x);
    b = a * a + sqrt(c * x);
    y = exp(2 * x) + pow(9.7, b);

    printf("x = %.1f, y = %.2f\n", x, y);

    A = (int)a;
    B = (int)b;
    C = (int)y;

    usl1 = (A % 2 == 0) != (B % 2 == 0);
    usl2 = (A % 3 == 0) && (B % 3 == 0) && (C % 3 == 0);

    printf("Только одно из чисел A и B четное, условие выполнено (1 - да, 0 - нет): %d\n", usl1);
    printf("Каждое из чисел A, B, C кратно трем, условие выполнено (1 - да, 0 - нет): %d\n", usl2);

    system("pause");
    return 0;
}
```
## Результат
задание 1
```
Введите угол в градусах
30
sin(30 град) = 0,500000
Введите угол в градусах
60
sin(60 град) = 0,866025
Введите угол в градусах
90
sin(90 град) = 1,000000
```
задание 2 и 3 
```
Введите x
3,5
x = 3,5, y = 1125,45 
Только одно из чисел A и B четное, условие выполнено (1 - да, 0 - нет): 1
Каждое из чисел A, B, C кратно трем, условие выполнено (1 - да, 0 - нет): 0
```
значение `y` совпадает с контр. примером
## Выполнила
Бакатанова Алла бИД-261 пдг2
