---
layout: post
title:  "Koni Hacmi Bulan C Kodu"
date:   2021-02-05 23:58:09 +0300
categories: problem-solving
---

***SORU :***

Klavyeden çap ve yükseklik bilgisi girilen koninin hacmini hesaplayan programı yazın.

***ÖRNEK :***    
    
Koninin capini giriniz = 
1

Koninin yuksekligini giriniz = 
1

Koninin hacmi = 1.047300
    
***AÇIKLAMA :***

Klavyeden girilecek olan çap ve yükseklik değerleri için, koninin hacmini hesaplamak için PI ve hesaplanacak hacim bilgisi için değişkenleri tanımlıyoruz. 

    float kcap,kyukseklik,khacim;
    float PI=3.1419;

Klavyeden almamız gereken değerleri alıyoruz.

    printf("Koninin capini giriniz = \n");
    scanf("%f",&kcap);

    printf("Koninin yuksekligini giriniz = \n");
    scanf("%f",&kyukseklik);

Hacim bilgisini hesaplayıp yazdırıyoruz.

    khacim = PI*kcap*kcap*kyukseklik/3;

    printf("Koninin hacmi = %f",khacim);


***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        float kcap;
        float kyukseklik;
        float PI=3.1419;
        float khacim;

        printf("Koninin capini giriniz = \n");
        scanf("%f",&kcap);

        printf("Koninin yuksekligini giriniz = \n");
        scanf("%f",&kyukseklik);

        khacim = PI*kcap*kcap*kyukseklik/3;

        printf("Koninin hacmi = %f",khacim);

        return 0;
    }