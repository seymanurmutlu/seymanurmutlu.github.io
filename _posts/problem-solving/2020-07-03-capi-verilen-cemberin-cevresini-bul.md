---
layout: post
title:  "Çapı girilen bir çemberin çevresini bulan C kodu"
date:   2020-07-23 14:46:09 +0300
categories: problem-solving
---
***SORU :***
    Çapı girilen bir çemberin çevresini bulan kodu yazınız.
    (pi=3.14)

***ÖRNEK :***

    Cemberin capini giriniz: 10.7
    ----------------------------
    Cemberin uzunlugu: 33.60

***AÇIKLAMA :***

Bu soruda ondalıklı sayılarla işlem yapacağımız için float veri tipini kullanmalıyız. Çember çevresini ve çember çapını tutacak iki float değişken tanımlıyoruz.

        float circleDiameter,circumference;

Çemberin çapını klavyeden girdi olarak alıp çemberin çevresini hesaplıyoruz. 

        printf("Cemberin capini giriniz: ");
        scanf("%f",&circleDiameter);

        circumference=2*(3.14)*circleDiameter;

Çemberin uzunluğunu yazdırırken sadece virgülden sonraki iki basamağı yazdırmak için *%.2f* şeklinde bastırdık.

        printf("---------------------------");
        printf("\nCember uzunlugu: %.2f",circumference);

***KOD :*** 

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        float circleDiameter,circumference;

        printf("Cemberin capini giriniz: ");
        scanf("%f",&circleDiameter);

        circumference=(3.14)*circleDiameter;
        printf("---------------------------");
        printf("\nCember uzunlugu: %.2f",circumference);

        return 0;
    }
    