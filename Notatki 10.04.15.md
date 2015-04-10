# Języki Programowania
1. Zadania:

2. Wykonać program do obliczania dat Wielkanocy w latach metodą Meeusa :smile:

3. #include <stdio.h>
4. void wielkanoc(int rok,swieta[]){
5. int a,b,c,d,e,f,g,h,i,j,k,l,m,p;
6. int dzien, swieta;
7. a=rok%19;
8. b=rok/100;
9. c=rok%100;
10. d=b/4;
11. e=b%4;
12. f=(b+8)/25;
13. g=(b-f+1)/3;
14. h=((19*a)+b-d-g+15)%30;
15. i=c/4;
16. k=c%4;
17. l=(32+(2*e)+(2*i)-h-k)%7;
18. m=(a+(11*h)+(22*l))/451;
19. p=(h+l-(7*m)+114)%31;
20. dzien=p+1;
21. miesiac=(h+l-(7*m)+114)/31;
22. swieta[0]=dzien;
23. swieta[1]=miesiac;
24. int main(void){
25. int rok;
26. int swieta[2];
27. printf("Podaj rok:");
28. scanf("%d",&rok);
29. wielkanoc(rok,swieta);
30. printf("Wielkanoc w %d roku wypada %d.%d (wg kalendarza gregorianskiego).",rok, swieta[0],swieta[1]);
31. return 0;
32. }

KONIEC :smile: :smile: :smile:
