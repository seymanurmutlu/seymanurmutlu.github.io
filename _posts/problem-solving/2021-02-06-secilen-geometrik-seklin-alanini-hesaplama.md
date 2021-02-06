---
layout: post
title:  "Seçilen Geometrik Şeklin Alanını Hesaplama (Switch Case)"
date:   2021-02-06 23:35:09 +0300
categories: problem-solving
---

***SORU :***

Klavyeden girilen seçime göre istenilen geometrik şeklin alanını hesaplayan programı yazınız.

***ÖRNEK :***    

    -----MENU-----
    (D veya d) Daire
    (T veya t) Diktortgen
    (K veya k) Kare
    (U veya u) Ucgen

    SECIMINIZ: d
    Dairenin yaricap uzunlugunu girin:11

    dairenin yaricap uzunlugu: 11
    dairenin alani: 379.94          
 
***KOD :***

    include <stdio.h>
    #include <stdlib.h>

    int main()
    {

        char secim;
        int uzunluk1,uzunluk2;

        printf("-----MENU-----\n");
        printf("(D veya d) Daire\n");
        printf("(T veya t) Diktortgen\n");
        printf("(K veya k) Kare\n");
        printf("(U veya u) Ucgen\n");
        printf("--------------------\n");
        printf("SECIMINIZ: ");
        scanf("%c",&secim);
        
        switch(secim){

            case 'D' :
            case 'd' :
                printf("Dairenin yaricap uzunlugunu girin:");
                scanf("%d",&uzunluk1);
                float dairealan=(3.14)*uzunluk1*uzunluk1;
                printf("\ndairenin yaricap uzunlugu: %d\n",uzunluk1);
                printf("dairenin alani: %.2f",dairealan);
            break;

            case 'T' :
            case 't' :
                printf("Diktortgenin kisa ve uzun kenar uzunluklarini girin:");
                scanf("%d %d",&uzunluk1,&uzunluk2);
                float dikdortgenalan=uzunluk1*uzunluk2;
                printf("\ndikdortgenin kisa kenar uzunlugu: %d \nuzun kenar uzunlugu: %d",uzunluk1,uzunluk2);
                printf("\ndikdortgenin alani: %.2f",dikdortgenalan);
            break;

            case 'K' :
            case 'k' :
                printf("Karenin bir kenarini girin:");
                scanf("%d",&uzunluk1);
                float karealan=uzunluk1*uzunluk1;
                printf("\nkarenin bir kenar uzunlugu: %d",uzunluk1);
                printf("\nkarenin alani: %.2f",karealan);
            break;

            case 'U' :
            case 'u' :
                printf("Ucgenin bir kenarinin uzunlugunu ve yuksekligini girin:");
                scanf("%d %d",&uzunluk1,&uzunluk2);
                float ucgenalan=(uzunluk1*uzunluk2)/2;
                printf("\nucgenin kenar uzunluguve yuksekligi: %d %d",uzunluk1,uzunluk2);
                printf("\nucgenin alani: %.2f",ucgenalan);
            break;

            default:
                printf("\nYanlis karakter girdiniz.\n");
            }
    
        return 0;
    }