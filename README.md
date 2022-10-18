#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <locale.h>
#include <math.h>

int main(void)
{
	setlocale(LC_ALL, "RUS");

	int years;
	puts("Ввести год:");
	scanf("%d", &years);
	
	if (years % 4 == 0) printf("високосный\n");
	else printf("не високосный\n");

	if ((years % 4 == 0) && (years % 100 != 0) || (years % 400 == 0)) printf("високосный\n");
	else printf("не високосный\n");

	printf(" %d год - %s", years, (years% 4 == 0 && years % 100 != 0) || (years % 400 == 0)?"високосный\n":
	"невисокосный\n");


	float x, y;
	puts("Ввести значение x\n");
	scanf("%f", &x);
	puts("Ввести значение y\n");
	scanf("%f", &y);
	if (!(x > y)) printf("F(%f, %f) = %lf\n", x, y, 2 * x + pow(y, 2));
	if (!(x == y)) printf("F(%f, %f) = %d\n", x, y, 100);
	if (!(x < y)) printf("F(%f,%f) = %lf\n", x, y, pow(x, 1 / y));


	float a;  //x ошибка, так как переменная уже объявлена выше
	puts("Введите значение a");
	scanf("%f", &a);
	if (a <= 7) printf("F(%f)=%f\n", a, -3 * a + 9);
	if (a > 7) printf("F(%f)=%lf\n", a, 1 / (a - 7));


	printf("F(%f)=%lf\n", a, (a <= 7) ? -3 * a + 9 : 1 / (a - 7));




