---
layout: post
title:  "İnç - cm - mm çeviricisi C kodu"
date:   2020-07-23 23:12:09 +0300
categories: problem-solving
---

***SORU :***

Klavyeden inç cinsinden girilen uzunlugu cm ve mmye ceviren programı yazın. (1 inc 2,54cm)

***ÖRNEK :***    
    
    Uzunluk(inc)= 1
    -----------------------------------
    1.00 inc = 2,54 cm = 25,40 mm
    
***AÇIKLAMA :***

Klavyeden inç değerini ve hesaplanacak cm, mm değerleri float değişkenleri tanımlıyoruz.

    float uzInc,uzCm,uzMm;

Klavyeden almamız gerekenleri değerleri alıyoruz.

    printf("Uzunluk(inc)=");
    scanf("%f",&uzInc);

Dönüşümleri hesaplayıp yazdırıyoruz.

    uzCm=(2.54)*uzInc;
    uzMm=uzCm*10;

    printf("--------------------------------\n");
    printf("%.2f inc = %.2f cm = %.2f mm\n\n",uzInc,uzCm,uzMm);

***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        float uzinc,uzcm,uzmm;

        printf("Uzunluk(inc)=");
        scanf("%f",&uzinc);

        uzcm=(2.54)*uzinc;
        uzmm=uzcm*10;

        printf("--------------------------------\n");
        printf("%.2f inc = %.2f cm = %.2f mm\n\n",uzinc,uzcm,uzmm);

        return 0;
    }