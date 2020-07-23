---
layout: post
title:  "Koordinat düzleminde verilen iki noktanın ortasını bulan C kodu"
date:   2020-07-24 00:14:09 +0300
categories: jekyll update
---

***SORU :***

Koordinat düzleminde girilen iki noktanın ortasını bulan programı yazınız.

***ÖRNEK :***    
    
    1.noktanin koordinatlarini giriniz (x y) = 
    5 5
    2.noktanin koordinatlarini giriniz (x y) =
    0 0 
    Orta noktanin koordinatlari = 2.500000 , 2.500000


***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        float x1,x2,y1,y2;
        float midX,midY;  //iki tam sayinin ortalamasi kesirli sayi olabilecegi icin float.

        printf("1.noktanin koordinatlarini giriniz (x y) = \n");
        scanf("%f %f",&x1,&y1);

        printf("2.noktanin koordinatlarini giriniz (x y) = \n");
        scanf("%f  %f",&x2,&y2);

        midX=(x1+x2)/2;
        midY=(y1+y2)/2;

        printf("Orta noktanin koordinatlari = %f , %f",midX,midY);

        return 0;
    }