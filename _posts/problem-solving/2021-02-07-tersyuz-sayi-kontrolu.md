---
layout: post
title:  "Tersyüz Sayı Özelliğini Kontrol Eden C Kodu"
date:   2021-02-07 11:37:15 +0300
categories: problem-solving
---

***SORU :***

Dört basamakli (abcd) pozitif tamsayilardan, ilk iki basamagi ile son iki basamağının çarpımı, rakamların yer değiştirilmiş halinin çarpımına eşit olma (ab*cd=ba*dc) özelliğine sahip olanlara Tersyüz Sayı denildiğini varsayınız. Klavyeden girilen dört basamaklı bir sayının Tersyüz olup olmadığını ekrana yazdiran programı yazınız.


***ÖRNEK :***    

    Dort basamakli sayiyi giriniz= 6213
    Binler basamagi: 6
    Yuzler basamagi: 2
    Onlar basamagi:  1
    Birler basamagi: 3
    Tersyuz sayidir.  

  
    Dort basamakli sayiyi giriniz= 1234
    Binler basamagi: 1
    Yuzler basamagi: 2
    Onlar basamagi:  3
    Birler basamagi: 4
    Tersyuz sayi degildir.
    
    
***AÇIKLAMA :***

Girilen sayının basamak değerlerini alıyoruz.

    int birler=sayi%10;
    int onlar=(sayi%100-birler)/10;
    int yuzler=(sayi%1000-onlar*10-birler)/100;
    int binler=sayi/1000;

Tersyüz sayı olma şartlarını kontrol ediyoruz.

    if((binler*10+yuzler)*(onlar*10+birler)==(yuzler*10+binler)*(birler*10+onlar))


***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {      
        
        int sayi;

        printf("Dort basamakli sayiyi giriniz= ");
        scanf("%d",&sayi);

        int birler=sayi%10;
        int onlar=(sayi%100-birler)/10;
        int yuzler=(sayi%1000-onlar*10-birler)/100;
        int binler=sayi/1000;

        printf("Binler basamagi: %d \n",binler);
        printf("Yuzler basamagi: %d \n",yuzler);
        printf("Onlar basamagi:  %d \n",onlar);
        printf("Birler basamagi: %d \n",birler);

        printf("------------------\n");
        if((binler*10+yuzler)*(onlar*10+birler)==(yuzler*10+binler)*(birler*10+onlar))
            printf("Tersyuz sayidir.\n");

        else printf("Tersyuz sayi degildir.\n");

        return 0;

    }