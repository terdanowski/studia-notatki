# Języki Programowania
# Zadanie 1:
Wykonać program do obliczania dat Wielkanocy w latach metodą Meeusa :smile:

1. #include <stdio.h>
2. void wielkanoc(int rok,swieta[]){
3. int a,b,c,d,e,f,g,h,i,j,k,l,m,p;
4. int dzien, swieta;
5. a=rok%19;
6. b=rok/100;
7. c=rok%100;
8. d=b/4;
9. e=b%4;
10. f=(b+8)/25;
11. g=(b-f+1)/3;
12. h=((19*a)+b-d-g+15)%30;
13. i=c/4;
14. k=c%4;
15. l=(32+(2*e)+(2*i)-h-k)%7;
16. m=(a+(11*h)+(22*l))/451;
17. p=(h+l-(7*m)+114)%31;
18. dzien=p+1;
19. miesiac=(h+l-(7*m)+114)/31;
20. swieta[0]=dzien;
21. swieta[1]=miesiac;
22. int main(void){
23. int rok;
24. int swieta[2];
25. printf("Podaj rok:");
26. scanf("%d",&rok);
27. wielkanoc(rok,swieta);
28. printf("Wielkanoc w %d roku wypada %d.%d (wg kalendarza gregorianskiego).",rok, swieta[0],swieta[1]);
29. return 0;
30. }

KONIEC :smile: :smile: :smile: kiedyś zacznie działać...

# Zadanie 2
Napisz pętlę while wypisującą na ekran znaki podane przez użytkownika, aż do napotkania znaku 'x'.

1. #include <stdio.h>
2. int main (){
3. 
