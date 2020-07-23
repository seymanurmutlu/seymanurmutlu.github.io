---
layout: post
title:  "Çapı girilen bir çemberin çevresini bulun"
date:   2017-09-23 14:46:09 +0300
categories: jekyll update
---
***SORU :***
    Çapı girilen bir çemberin çevresini bulan kodu yazınız.
    (pi=3.14)

***ÖRNEK :***

    Cemberin capini giriniz: 10.7
    ----------------------------
    Cemberin uzunlugu: xxx

***AÇIKLAMA :***

Bu soruda ondalıklı sayılarla işlem yapacağımız için float veri tipini kullanmalıyız. Çember uzunluğu ve çember çapını tutacak iki float değişken(float cembercap,cemberuz) tanımlıyoruz.

        float cembercap,cemberuz;

Çemberin çapını klavyeden girdi olarak alıp çemberin çevresini hesaplıyoruz. 

        printf("Cemberin capini giriniz: ");
        scanf("%f",&cembercap);

        cemberuz=2*(3.14)*cembercap;

Çemberin uzunluğunu yazdırırken sadece virgülden sonraki iki basamağı yazdırmak için *%.2f* şeklinde bastırdık.

        printf("---------------------------");
        printf("\nCember uzunlugu: %.2f",cemberuz);

***KOD :*** 

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        float cembercap,cemberuz;

        printf("Cemberin capini giriniz: ");
        scanf("%f",&cembercap);

        cemberuz=2*(3.14)*cembercap;
        printf("---------------------------");
        printf("\nCember uzunlugu: %.2f",cemberuz);

        return 0;
    }
    