# <li><a href="http://iftia9.univ.gda.pl/~pg/">dr P.Gnaciński</a>

### **I. PĘTLE**

**Zad. 1.** Wypisz liczby calkowite od 0 do 23:

a) za pomoca petli for
```c
#include <stdio.h>
int main(){
	int n;
	for (n=0; n<=23; n=n+1)
		printf ("\n%d\n", n);      
	getchar ();    
	return 0; 
}
```
b) za pomoca petli while
```c
#include <stdio.h>
int main(){
	int n=0;
	while (n<=23){
		printf ("\n%d\n", n);
		n=n+1;
	}          
	getchar ();    
	return 0;
}
```
c) za pomoca petli do-while
```c
#include <stdio.h>
int main(){
	int n=0;
	do {
		printf ("%d\n", n);    
		n=n+1; 
	}
	while (n<=23); 
	getchar ();
}
```
**Zad. 2.** Wypisz liczby od -3.5 do 7.5 z krokiem co 0.5:

a) za pomoca petli for
```c
#include <stdio.h>
int main(){
	double n;
	for (n=-3.5; n<=7.5; n=n+0.5)
		printf ("%.1lf\n", n);      
	getchar ();    
	return 0; 
}
```
b) za pomoca petli while
```c
#include <stdio.h>
int main(){
	double n=-3.5;
	while (n<=7.5){
		printf ("%.1lf\n", n);
		n=n+0.5;
	}          
	getchar ();    
	return 0;
}
```
c) za pomoca petli do-while
```c
#include <stdio.h>
int main()
{
	double i,n;
	i=-3.5;
	n=7.5;
	do
	{ printf ("%.1lf\n", i);
	i=i+0.5;
	}
	while (i<=n);
	getchar(); getchar();
	return 0;
}
```
**Zad. 3.** Wczytaj n liczb i wyswietl ich sume i srednia arytmetyczna.
```c
#include<stdio.h>
int main(){
	int n,i;
	double x, suma=0.0, srednia;
	do{
		printf ("Podaj ilosc liczb (co najmniej 1): ");
		scanf ("%d", &n);
	}
	while (n<1);
	for (i=1;i<=n;i++){
		printf ("\nPodaj %d liczbe: ",i);
		scanf ("%lf", &x);
		suma=suma+x;
	}
	srednia=suma/n;
	printf ("\nSuma podanych %d liczb wynosi: %.3lf",n,suma);
	printf ("\n\nSrednia z podanych %d liczb wynosi: %.3lf",n,srednia);
	getchar();
	getchar();
	return 0;
}
```
**Zad. 4.** Wypisz kwadraty i szesciany liczb naturalnych od 1 do liczby podanej przez użytkownika:

a) za pomoca petli for
```c
#include <stdio.h>
int main ()
{
	int i, n;
	printf ("Podaj liczbe: ");
	scanf ("%d", &n);
	for (i = 1; i <= n; i++)
	{
		printf ("\n%d %d %d\n", i, i * i, i * i * i);
	}
	printf ("\n");
	getchar ();
	getchar ();
	return 0;
}
```
b) za pomoca petli while
```c
#include <stdio.h>
int main ()
{
	int i, n;
	printf ("Podaj liczbe: ");
	scanf ("%d", &n);
	i = 1;
	while (i <= n)
	{
		printf ("\n%d %d %d \n", i, i * i, i * i * i);
		i++;
	}
	printf ("\n");
	getchar ();
	getchar ();
	return 0;
}
```
c) za pomoca petli do-while
```c
#include <stdio.h>
int main ()
{
	int i, n;
	printf ("Podaj liczbe: ");
	scanf ("%d", &n);
	i = 1;
	do
	{
		printf ("\n%d %d %d \n", i, i * i, i * i * i);
		i++;
	}
	while (i <= n);
	getchar ();
	getchar ();
	return 0;
}
```
**Zad. 5.** Oblicz sume kwadratów liczb od 3 do 15:

a) za pomoca petli for
```c
# include <stdio.h>
int main (){
	int i;
	int suma=0;
	for (i=3; i<=15; i++)
	{
		suma = suma + (i*i);
	}
	printf ("Suma kwadratow liczb od 3 do 15: %d", suma);
	i=3;
	suma=0;
	getchar ();
	return 0;
}
```
b) za pomoca petli while
```c
# include <stdio.h>
int main (){
	int i;
	int suma=0;
	while (i<=15)
	{
		suma = suma + (i*i);
		i++;
	}
	printf ("Suma kwadratow liczb od 3 do 15: %d", suma);
	getchar ();
	return 0;
}
```
**Zad. 6.** Wypisz sinusy i cosinusy katów 0 ... 180 stopni z krokiem co 30 stopni za pomoca petli for.
```c
# include <stdio.h>
# include <math.h>
int main (){
	double x;
	for (x=0; x<=180; x=x+30){
		printf ("sin(%.0lf)=%.3lf\n", x, sin(x*M_PI/180));
		printf ("cos(%.0lf)=%.3lf\n", x, cos(x*M_PI/180));
	}
	getchar ();
	return 0;
}
```
**Zad. 7.** Wypisz znaki od 'a' do 'k' wraz z ich kodami ASCII (dziesietnie i szesnastkowo) w kolejnosci rosnacej i malejacej za pomoca petli for.
```c
# include <stdio.h>
int main (){
	char i;
	for (i=32; i<=127;i++) {
		printf ("Litera:%c   znak ASCII:%3d   szesnastkowo:%2x\n", i, i, i);
	}
	getchar ();
	return 0;
}
```
**Zad. 8.** Napisz petle while wypisujaca na ekran znaki podane przez użytkownika, aż do napotkania znaku 'x'.
```c
#include <stdio.h>
#define znak 'x'
int main() {
	char i='a';
	while(i!=znak)    {
		printf("Podaj litere: ");
		scanf("%c", &i);
		printf("Podales litere: %c \n\n",i);
		getchar();
	}
	printf("PODALES LITERE X - KONIEC PROGRAMU!");
	getchar();
	return 0;
}
```
**Zad. 9.** Napisz program wyswietlajacy tabliczke mnożenia do 13.
```c
#include <stdio.h>
int main ()
{
  int i, j;
  printf ("\n    |");
  for (i = 1; i <= 13; i++)
    {
      printf ("%4d ", i);
    }
  printf
    ("\n----|-----------------------------------------------------------------\n");
  for (i = 1; i <= 13; i++)
    {
      for (j = 1; j <= 13; j++)
        {
          if (j == 1)
            {
              printf ("\n%3d |", j * i);
            }
          printf ("%4d ", j * i);
        }
      putchar ('\n');
    }
  getchar ();
  return 0;
}
```

### **II. INSTRUKCJE WARUNKOWE**

**Zad. 1.** Napisz program liczacy pierwiastki trójmianu kwadratowego: a*x^2 + b*x + c=0.
```c
#include <math.h>
int main (){
	double a, b, c, delta, x1, x2;
	printf ("Podaj a: ");
	scanf ("%lf", &a);
	printf ("\nPodaj b: ");
	scanf ("%lf", &b);
	printf ("\nPodaj c: ");
	scanf ("%lf", &c);
	delta = b*b-4*a*c;
	printf ("\ndelta = %.3lf\n\n", delta);
	if (delta>0){
		x1 = (-b-sqrt(delta))/(2*a);
		x2 = (-b+sqrt(delta))/(2*a);
		printf ("MAMY DWA ROZWIAZANIA, BO DELTA JEST WIEKSZA NIZ 0.\n");
		printf ("\nx1 = %.3lf\n", x1);
		printf ("\nx2 = %.3lf", x2);
	}
	if (delta==0) {
		x1 = x2 = -b / (2*a);
		printf ("MAMY JEDNO ROZWIAZANIE, BO DELTA JEST ROWNA 0.\n");
		printf ("x1 = x2 = %.3lf", x1 = x2);
	}
	if (delta<0) {
		printf ("BRAK ROZWIAZAN, BO DELTA JEST MNIEJSZA NIZ 0.");
	}
	getchar ();
	getchar ();
	return 0;
}
```
**Zad. 2.** Znajdź liczby o tej wlasnosci, że suma dzielników wlasciwych liczby jest równa zadanej liczbie, np. 6=1+2+3. Sa to tak zwane liczby doskonale.
```c
# include <stdio.h>
# include <math.h>
int main (){
	int x;
	int d;
	int suma;
	int reszta;
	for (x=2; x<=10000; x++)
	{
		suma=0;
		for (d=1; d<x; d++)
		{
			reszta=x%d;
			if (reszta==0)
			{
				suma=suma+d;
			}
		}
		if (suma==x)
		{
			printf ("LICZBA %d JEST LICZBA DOSKONALA.\n", x);
		}
	}
	getchar ();
	getchar ();
	return 0;
}
```
**Zad. 3.** Wyswietl 20 różnych (tj. bez permutacji liczb) trójek pitagorejskich, tzn. takich liczb calkowitych dodatnich a, b i c, że a^2 + b^2 = c^2.
```c
# include <stdio.h>
# include <math.h>
int main (){
	int a;
	int b;
	int c;
	int licznik=1;
	for (a=1; a<=100; a++)
	{
		for (b=a; b<=100; b++)
			for (c=b; c<=100; c++)
			{
				if (a*a + b*b == c*c && licznik<=20)
				{
					printf ("\n\nTROJKA PITAGOREJSKA NR %d:", licznik);
					printf (" %d %d %d", a, b, c);
					licznik++;        
				}
			}
	}
	getchar ();
	getchar ();
	return 0;  
}
```
**Zad. 4.** Napisz program podajacy najwieksza i najmniejsza z podanych liczb zmiennoprzecinkowych.
```c
# include <stdio.h>
# include <math.h>
int main (){
	int k;
	int x;
	double n;
	double zero=0.0;
	double max=-1/zero;
	double min=1/zero;
	printf ("Podaj ilosc liczb (co najmniej 2): ");
	scanf ("%d", &k);
	for (x=1; x<=k; x++)
	{
		printf ("Podaj %d liczbe: ", x);
		scanf ("%lf", &n);
		if (n<min)
			min = n;
		if (n>max)
			max = n;
	}
	printf ("MAX = %.3lf", max);
	printf ("\nMIN = %.3lf", min);
	getchar ();
	return 0;
}
```
**Zad. 5.** Napisz program wypisujacy slownie dzień tygodnia, jeżeli nr dnia tygodnia jest znany jako liczba (np. 3). Użyj instrukcji switch-case.
```c
#include<stdio.h>
int main() {
	int liczba;
	printf("Wpisz liczbe, aby wyswietlic odpowiadajacy jej dzien tygodnia: ");
	scanf("%d",&liczba);
	switch(liczba)
	{
	case 1: 
		printf("\nPONIEDZIALEK :)");
		break; 
	case 2: 
		printf("\nWTOREK :)");
		break;
	case 3:
		printf("\nSRODA :)");
		break;
	case 4:
		printf("\nCZWARTEK :)");
		break;
	case 5:
		printf("\nPIATEK :)");
		break;
	case 6:
		printf("\nSOBOTA :)");
		break;
	case 7:
		printf("\nNIEDZIELA :)");
		break;
	default: printf("\nNIE MA TAKIEGO DNIA TYGODNIA :(");
		break;
	}
	getchar();
	getchar();
	return 0;
}
```

### **III. FUNKCJE**

**Zad. 1.** Napisz funkcję obliczającą pole kuli o podanym promieniu.
```c
#include <stdio.h>
#include <math.h>
double poleKuli(double r)
{
 return  4*M_PI*r*r;   
}
int main(){
	double r;     
	printf ("Podaj promien kuli: ");
	scanf ("%lf", &r);
	printf ("\nP = %d x %.3lf x %.0lf x %.0lf = %.3lf\n", 4, M_PI, r, r, poleKuli(r));
	getchar ();
	getchar ();
	return 0;
}
```
**Zad. 2.** Napisz funkcję wartoscBezwzgledna zwracająca wartość bezwzględną z liczby całkowitej.
```c
#include <stdio.h>
#include <ctype.h>
#define MAX 32
int main(){
 char napis[MAX];
	int c, i=0, end;
	puts ("Wpisz dowolny tekst: ");
	while ((c=getchar())!=EOF)
	{
		napis[i]=toupper(c);
		i++;
	}
	end=--i;
	for (i=0; i<=end; i++)
		printf ("%c", napis[i]); 
	getchar ();                 
	return 0;                 
}
```
**Zad. 3.** Napisz funkcję obliczającą a^n (n-liczba naturalna) za pomocą pętli.
```c
#include <stdio.h>
#include <math.h>
double potega(double a, int n);
int main() {
 double a;
	int n;
	double x;
	printf("Podaj liczbe: ");
	scanf("%lf",&a);
	printf("\nPodaj wykladnik (liczba naturalna): ");
	scanf("%d",&n);
	x=potega(a,n);
	printf("\n%.3lf do potegi %d rowna sie %.3lf ", a, n, x);
	getchar();
	getchar();
	return 0;
}   
double potega(double a, int n)
{
	int i;
	double x=1.0;
	for(i=1;i<=n;i++)
	{
		x=x*a;
	}
	return x;
}
```
**Zad. 4.** Napisz funkcję obliczającą pierwiastek z a algorytmem Herona.
```c
#include <stdio.h>
#include <math.h>
double Heron (double a)
{
 double x=1, eps=1e-15;
	do
	{
		x=0.5*(x+(a/x));
	}
	while (fabs(x-a/x)>eps*x);
	return x;
}
int main(){
	double a;
	double x=1;
	double z;
	printf ("Podaj liczbe: ");
	scanf ("%lf", &a);
	for (z=1e-5; z<=1e15; z=z*10)
	{
		printf ("\nHeron(%lf)=%.15lf\n", z, Heron(a));
		printf ("\nsqrt(%lf)=%.15lf\t", z, sqrt(a));
		printf ("\n\nblad wzgledny=%.15le", (Heron(a)-sqrt(a))/sqrt(a));
		getchar ();
		getchar ();
		return 0;
	}
}
```
**Zad. 5.** Napisz funkcje do szybkiego obliczania a^n.
```c
#include <stdio.h>
int potegaAn (int a, int n);
int main (){
 int a, p, n;
	printf ("Podaj liczbe naturalna: ");
	scanf ("%d", &a);
	printf ("\nPodaj wykladnik (liczba naturalna): ");
	scanf ("%d", &n);
	p = potegaAn (a, n);
	printf ("\nWartosc %d do potegi %d wynosi %d", a, n, p);
	getchar ();
	getchar ();
	return 0;
}
int
	potegaAn (int a, int n)
{
	int i = n, p = 1, q = a;
	while (i > 0)
	{
		if (i % 2 != 0)
			p = p * q;
		q = q * q;
		i = i / 2;
	}
	return p;
}
```
**Zad. 6.** Napisz funkcje do szybkiego obliczania a^n (n-liczba cakowita, a-typ double).
```c
#include <stdio.h>
double potegaAn (double a, int n);
int main () {
 int n;
	double a, p;
	printf ("\nPodaj liczbe: ");
	scanf ("%lf", &a);
	printf ("\nPodaj wykladnik (liczba naturalna): ");
	scanf ("%d", &n);
	p = potegaAn (a, n);
	printf ("\nWartosc %lf do potegi %d wynosi %lf", a, n, p);
	getchar ();
	getchar ();
	return 0;
}
double potegaAn (double a, int n)
{
	int i = n, minus = 0;
	double p = 1.0, q = a;
	if (i < 0)
	{
		minus = 1;
		i = -i;
	}
	while (i > 0)
	{
		if (i % 2 != 0)
			p = p * q;
		q = q * q;
		i = i / 2;
	}
	if (minus == 0)
		return p;
	else
		return (1.0 / p);
}
```

### **IV. TABLICE**

**Zad. 1.** Wypisz wszystkie elementy tablicy: int dane[]={-44, 5, 67, -2, 0, 33, 77} w kolejności od pierwszego do ostatniego i odwrotnie.
```c
#include <stdio.h>
#include <math.h>
int main (){
	int dane[]={-44, 5, 67, -2, 0, 33, 77};
	int i;
	int max=6;
	for(i=0; i<=max; i++)
		printf("%d,", dane[i]);
	for(i=max; i>=0; i--)
		printf("%d,", dane[i]);
	getchar();
	return 0;
}
```
**Zad. 2.** Napisz program, który podany tekst wyświetli wielkimi literami.
```c
#include <stdio.h>
#include <ctype.h>
#include <string.h>
int main(){
	int i;   
	char napis[]="ania";
	for (i=0; i<strlen(napis); i++)
	{
		napis[i]=toupper(napis[i]);
	}
	printf (napis);
	getchar ();
	return 0;
}
```
**Zad. 3.** Napisz funkcje sprawdzajaca, czy podana przez użytkownika liczba znajduje sie w powyższej tablicy.
```c
#include <stdio.h>
#include <string.h>
int main (){
	int i;
	int x;
	int y=0;
	int TABLICA [100]={2,4,6,8,10,12,14,16,18};
	printf ("\nWprowadz liczbe: ");
	scanf ("%d", &x);
	for (i=0; i<sizeof (TABLICA)/sizeof (TABLICA [0]); i++)
	{
		if (TABLICA [i]==x)
			y++;
	}
	if (y>0)
	{
		printf("\nPODANA LICZBA ZNAJDUJE SIE W TABLICY :)");
	}
	else
		printf("\nPODANA LICZBA NIE ZNAJDUJE SIE W TABLICY :(");
	getchar ();
	getchar ();
	return 0;
	for (i=0; i<100; i++)
	{
		printf ("%d", TABLICA [i]);
	}
	getchar ();
	return 0;
}
```
**Zad. 4.** Znajdź maksymalna liczbe w tablicy liczb zmiennoprzecinkowych podanych przez użytkownika.
```c
#include <stdio.h>
#define rozmiar 5               
double emax (double dane[]);    
int main () {
	double dane[rozmiar];
	double x;
	double max;
	int i;
	for (i = 0; i < rozmiar; i++) 
	{
		printf ("\nWprowadz liczbe nr %d: ", i + 1);
		scanf ("%lf", &x);
		dane[i] = x;
	}
	max = emax (dane);            
	for (i = 0; i < rozmiar; i++) 
		printf ("\nElemnt %d tablicy ma wartosc: %lf\n", i, dane[i]);
	printf ("\nElemnt najwiekszy z tablicy to: %lf", max);     
	getchar ();
	getchar ();
	return 0;
}
double emax (double dane[])            
{
	int i;
	double max = dane[0];        
	for (i = 0; i < rozmiar; i++)
	{
		if (dane[i] >= max)
			max = dane[i];
	}
	return max;
}
```
**Zad. 5.** Napisz funkcje obliczajaca srednia arytmetyczna z liczb zawartych w tablicy liczb zmiennoprzecinkowych.
```c
#include <stdio.h>
#define rozmiar 5
double esrednia (double dane[], int n);        
int main () {
	double dane[rozmiar];
	double x;
	double srednia;
	int i;
	for (i = 0; i < rozmiar; i++)
	{
		printf ("\nWprowadz liczbe nr %d: ", i + 1);
		scanf ("%lf", &x);
		dane[i] = x;
	}
	srednia = esrednia (dane, rozmiar);
	for (i = 0; i < rozmiar; i++)
		printf ("\nElemnt %d tablicy ma wartosc: %lf\n", i, dane[i]);
	printf ("\nSrednia to: %lf", srednia);
	getchar ();
	getchar ();
	return 0;
}
double esrednia (double dane[], int n)
{
	int i;
	double x;
	double suma = 0.0;
	for (i = 0; i < n; i++)
		suma += dane[i];
	return suma / rozmiar;
}
```
**Zad. 6.** Wypisz napis: char tekst [] = "Tablice to podstawa programowania." od końca do poczatku.
```c
#include <stdio.h>
int main () {
	char tekst[] = "Tablica to podstawa programowania.";
	int rozmiar = sizeof (tekst) / sizeof (char), i, j = rozmiar - 1;
	char rewers[rozmiar];
	for (i = 0; i < rozmiar; i++, j--)
		rewers[i] = tekst[j];
	for (i = 0; i < rozmiar; i++)
		printf ("%c", rewers[i]);
	getchar ();
	return 0;
}
```
**Zad. 7.** Napisz funkcje void odKonca (char napis []) która odwraca podany napis (taka funkcja jest potrzebna np. do zamiany liczby na system dwójkowy).
```c
#include <stdio.h>
#include <string.h>
#define rozmiar 32
void odKonca (char napis[]);
int main () {
	char napis[rozmiar];
	char c;
	int i;
	for (i = 0; i < rozmiar; i++) 
		napis[i] = '\0';
	i = 0;
	printf ("\nWprowadz napis: ");   
	while ((c = getchar ()) != '\n')
	{
		napis[i] = c;
		i++;
	}
	napis[i]='\0';                  
	printf ("\n%s\n\n", napis);       
	odKonca (napis);              
	printf (napis);                  
	getchar ();
	return 0;
}
void odKonca (char napis[])          
{
	int i;
	int j = strlen(napis) - 1;
	char rewers[strlen(napis)];
	for (i = 0; i < strlen(napis); i++, j--)
		rewers[i] = napis[j];
	for (i = 0; i < strlen(napis); i++)
		napis[i] = rewers[i];
}
```
**Zad. 8.** Napisz funkcje zwracajaca najmniejszy i najwiekszy element z tablicy liczb zmiennoprzecinkowych podanej jako argument funkcji.
```c
#include <stdio.h>
#define rozmiar 5
struct minMax {
	double min;
	double max;
};
struct minMax extr (double dane[], int n);    
int main () {
	double dane[rozmiar];
	double x;
	double min;
	double max;
	int i;
	struct minMax mM;
	for (i = 0; i < rozmiar; i++)
	{
		printf ("\nWprowadz liczbe nr %d: ", i + 1);
		scanf ("%lf", &x);
		dane[i] = x;
	}
	for (i = 0; i < rozmiar; i++)
		printf ("\nElemnt %d tablicy ma wartosc: %lf\n", i, dane[i]);
	mM = extr (dane, rozmiar);
	printf ("\nElement najmniejszy to: %lf\n\nElement najwiekszy to: %lf",mM.min, mM.max);
	getchar ();
	getchar ();
	return 0;
}
struct minMax extr (double dane[], int n)
{
	int i;
	double x;
	double min;
	double max;
	struct minMax mM;
	min = max = dane[0];
	for (i = 1; i < n; i++)
	{
		x = dane[i];
		if (x <= min)
			min = x;
		if (x >= max)
			max = x;
	}
	mM.min = min;
	mM.max = max;
	return mM;
}
```
**Zad. 9.** Napisać program, który pobiera od użytkownika n liczb i wczytuje je do tablicy. Napisać funkcje, która zwróci ostatnia liczbe tej tablicy podzielna przez 7.
```c
#include <stdio.h>
#define rozmiar 5
int jest7 (int dane[]);
int main () {
	int dane[rozmiar];
	int i;
	int x;
	int a;
	for (i = 0; i < rozmiar; i++)
	{
		printf ("\nWprowadz liczbe nr %d: ", i + 1);
		scanf ("%d", &x);
		dane[i] = x;
	}
	for (i = 0; i < rozmiar; i++)
		printf ("\nElemnt %d tablicy ma wartosc: %d\n", i, dane[i]);
	a = jest7 (dane);
	if (a == 1)
		printf ("\n\nNie wystepuje liczba podzielna przez 7");
	else
		printf ("\nOstatnia podana liczba podzielna przez 7 to: %d", a);
	getchar ();
	getchar ();
	return 0;
}
int jest7 (int dane[])
{
	int i;
	int x;
	int a = 1;
	for (i = 0; i < rozmiar; i++)
		if (dane[i] % 7 == 0)
			a = dane[i];
	return a;
}
```
**Zad. 10.** Napisz funkcje obliczajaca iloczyn skalarny dwóch wektorów n-wymiarowych.
```c
#include <stdio.h>
#define N 10                     
double iloczyn (double dane1[], double dane2[], int n);
void wysWekt(double dane[], int n);
void wprWekt(double dane[], int n);
int main () {
	double dane1[N];
	double dane2[N];
	double x;
	int i;
	int n;
	printf ("\nWprowadz rozmiar wektorow: ");
	scanf ("%d", &n);
	printf ("\nWprowadz skladowe pierwszego wektora:\n");
	wprWekt(dane1, n);
	puts (" ");  
	printf ("Wprowadz skladowe drugiego wektora:\n");
	wprWekt(dane2, n);
	printf ("\nWektor pierwszy = ");
	wysWekt(dane1, n);
	printf ("\n\nWektor drugi = ");
	wysWekt(dane2, n);
	x = iloczyn (dane1, dane2, n);   
	printf ("\n\nIloczyn skalarny tych wektorow wynosi = %lf.", x);
	getchar ();
	getchar ();
	return 0;
}
double iloczyn (double dane1[], double dane2[], int n)        
{
	int i;
	double x = 0.0;
	for (i = 0; i < n; i++)
		x += (dane1[i]) * (dane2[i]);
	return x;
}
void wysWekt(double dane[], int n)
{
	int i;
	printf ("[");
	for (i = 0; i < n; i++)
	{
		printf ("%lf", dane[i]);
		if (i < n - 1)
			printf (",");
	}
	printf ("].");
}
void wprWekt(double dane[], int n)
{
	int i;
	double x;
	for (i = 0; i < n; i++)       
	{
		printf ("\nnr %d: ", i + 1);
		scanf ("%lf", &x);
		dane[i] = x;
	}
}
```
**Zad. 11.** Napisz funkcje, która transponuje tablice kwadratowa double tab [128] [128] podana jako argument. Napisz i wykorzystaj funkcje void wyswietlMacierz (double m [128] [128], int wierszy, int kolumn);
```c
#include <stdio.h>
#define N 128                     
double trans (double tab[N][N], int wierszy, int kolumn);
void wyswietlMacierz (double m[N][N], int wierszy, int kolumn);
int main () {
	double tab[N][N];
	double tabT[N][N];
	double x;
	int i;
	int j;
	int wierszy;
	int kolumn;
	printf ("\nWprowadz ilosc wierszy: ");
	scanf ("%d", &wierszy);
	printf ("\nWprowadz ilosc kolumn: ");
	scanf ("%d", &kolumn);          
	for (i = 0; i < wierszy; i++)       
	{
		for (j = 0; j < kolumn; j++)   
		{
			printf ("\nWprowadz skladowa tablicy [%d,%d]: ", i + 1, j + 1);
			scanf ("%lf", &x);
			tab[i][j] = x;
		}
	}
	printf ("\n");         
	wyswietlMacierz (tab, wierszy, kolumn);
	printf ("\n");             
	for (i = 0; i < wierszy; i++)       
		for (j = 0; j < kolumn; j++)
			tabT[i][j] = tab[i][j];
	trans (tabT, wierszy, kolumn);
	wyswietlMacierz (tabT, kolumn, wierszy); 
	getchar ();
	getchar ();
	return 0;
}
double trans (double tab[N][N], int wierszy, int kolumn)
{
	double tabT[N][N];
	int i;
	int j;
	int k;
	for (i = 0; i < wierszy; i++)       
		for (j = 0; j < kolumn; j++)
			tabT[j][i] = tab[i][j];
	for (i = 0; i < kolumn; i++)      
		for (j = 0; j < wierszy; j++)
			tab[i][j] = tabT[i][j];
}
void wyswietlMacierz (double m[N][N], int wierszy, int kolumn)
{
	int i;
	int j;
	for (i = 0; i < wierszy; i++)
		for (j = 0; j < kolumn; j++)
			printf ("%lf %c", m[i][j], j == kolumn - 1 ? '\n' : ' ');
}
```
**Program obliczajacy droge zatrzymania**
```c
#include <stdio.h>
double wprV ();
int wprX ();
int wprY ();
double ustalU (int z);
void wypisz (char znak);
double drogaH (double V, double u, double g);
double drogaR (double V, double t);
int main (){
	int x, y = 0, z;
	double V, u, g = 9.80665;
	double s, s1, s2, s3;
	double t1 = 0.85, t2 = 0.5;
	char znak1 = '-', znak2 = '*';
	wypisz (znak1);
	V = wprV ();
	wypisz (znak1);
	printf ("\nWiedzac, ze: \n\n1 - beton \n\n2 - asfalt \n\n3 - kostka kamienna czysta \n\n4 - kostka kamienna zakurzona \n\n5 - klinkier \n\n6 - droga gruntowa twarda \n\n7 - zwir \n\n8 - droga pokryta sniegiem \n\n9 - droga oblodzona \n\n");
	wypisz (znak1);
	x = wprX ();
	wypisz (znak1);
	if (x <= 6)
	{
		printf ("\nWiedzac, ze: \n\n1 - suchy/sucha \n\n2 - mokry/mokra \n\n");
		wypisz (znak1);
		y = wprY ();
		wypisz (znak1);
	}
	z = 10 * x + y;
	u = ustalU (z);
	wypisz (znak2);
	s1 = drogaH (V, u, g);
	s2 = drogaR (V, t1);
	s3 = drogaR (V, t2);
	s = s1 + s2 + s3;
	printf ("\nDroga hamowania wynosi %.3lf m", s1);
	printf ("\n\nDroga wynikajaca z czasu reakcji kierowcy wynosi %.3lf m", s2);
	printf ("\n\nDroga wynikajaca z czasu reakcji ukladu hamulcowego wynosi %.3lf m", s3);
	wypisz (znak2);
	printf ("\nDROGA ZATRZYMANIA WYNOSI WIEC OKOLO %.0lf m", s);
	wypisz (znak2);
	getchar ();
	return 0;
}
void wypisz (char znak)
{
	int i;
	if (znak == '*')
		printf ("\n\n");
	for (i = 1; i <= 67; i++)
		printf ("%c", znak);
	printf ("\n");
}
double wprV ()
{
	double V;
	do
	{
		printf ("\nPodaj predkosc w km/h: ");
		scanf ("%lf", &V);
		printf ("\n");
	}
	while (V <= 0 || V > 1500);
	return V;
}
int wprX ()
{
	int x;
	do
	{
		printf ("\nPodaj cyfre okreslajaca rodzaj nawierzchni: ");
		scanf ("%d", &x);
		printf ("\n");
	}
	while (x < 1 || x > 9);
	return x;
}
int wprY ()
{
	int y;
	do
	{
		printf ("\nPodaj cyfre okreslajaca stan okreslonej wczesniej nawierzchni: ");
		scanf ("%d", &y);
		printf ("\n");
	}
	while (!(y == 1 || y == 2));
	return y;
}
double ustalU (int z)
{
	int i;
	double u;
	double tablica[15][2] = { {0.94,11} , {0.5,12} , {0.89,21} , {0.5,22} , {0.75,31} , {0.45,32} , {0.65,41} , {0.3,42} , {0.75,51} , {0.45,52} , {0.55,61} , {0.35,62} , {0.45,70} , {0.25,80} , {0.1,90} };
	for (i=0; i<15; i++)
	{
	if (z == tablica[i][1])
	u = tablica[i][0];
    }
	return u;
}
double drogaH (double V, double u, double g)
{
	double s;
	s = ((V / 3.6) * (V / 3.6)) / (2 * u * g);
	return s;
}
double drogaR (double V, double t)
{
	double s;
	s = (t * V) / 3.6;
	return s;
}
```
