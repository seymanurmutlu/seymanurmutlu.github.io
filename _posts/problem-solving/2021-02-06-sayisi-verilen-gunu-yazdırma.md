---
layout: post
title:  Sayısı Verilen Günü Yazdırma (Switch Case)
date:   2021-02-06 23:32:09 +0300
categories: problem-solving
---

***SORU :***
Klavyeden girilen sayiya gore gunu haftanın hangi günü olduğunu veren program.

***ÖRNEK :***    

Gunun degerini giriniz[1-7]: 1
Girdiginiz deger 'Pazar' a aittir.
    
***AÇIKLAMA :***

İhtiyacımız olan gün sayısı için değişken tanımlıyoruz.
    
    int gununsayisi;

Klavyeden almamız gerekenleri değerleri alıyoruz.

    printf("Gunun degerini giriniz[1-7]: ");
    scanf("%d",&gununsayisi);

Switch case yapısını kuruyoruz. Günün sayısına göre karar mekanizmasını oluşturacağımız için swicth içerisine klavyeden aldığımız değişkeni yazıyoruz. Değişkenin 1 ile 7 arasında bir değer alması durumunda günü yazdıracak şeklinde yapıyı kuruyoruz. 1-7 arasında her hangi bir tam sayı değeri girilmemesi durumunda yanlış değer girilmiş olacağından dolayı default kısmını bu kontrol mekanizması için kullanıyoruz.

    switch(gununsayisi){

        case 1 :
            printf("Girdiginiz deger 'Pazar' a aittir.");
        break;

        case 2 :
            printf("Girdiginiz deger 'Pazartesi' ye aittir.");
        break;

        case 3 :
            printf("Girdiginiz deger 'Salý' ya aittir.");
        break;

        case 4 :
            printf("Girdiginiz deger 'Carsamba' ya aittir.");
        break;

        case 5 :
            printf("Girdiginiz deger 'Persembe' ye aittir.");
        break;

        case 6 :
            printf("Girdiginiz deger 'Cuma' ya aittir.");
        break;

        case 7 :
            printf("Girdiginiz deger 'Cumartesi' ye aittir.");
        break;

        default:
            printf("Yanlis deger girdiniz.");
    }

***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        int gununsayisi;
        printf("Gunun degerini giriniz[1-7]: ");
        scanf("%d",&gununsayisi);

    switch(gununsayisi){

        case 1 :
            printf("Girdiginiz deger 'Pazar' a aittir.");
        break;

        case 2 :
            printf("Girdiginiz deger 'Pazartesi' ye aittir.");
        break;

        case 3 :
            printf("Girdiginiz deger 'Salý' ya aittir.");
        break;

        case 4 :
            printf("Girdiginiz deger 'Carsamba' ya aittir.");
        break;

        case 5 :
            printf("Girdiginiz deger 'Persembe' ye aittir.");
        break;

        case 6 :
            printf("Girdiginiz deger 'Cuma' ya aittir.");
        break;

        case 7 :
            printf("Girdiginiz deger 'Cumartesi' ye aittir.");
        break;

        default:
            printf("Yanlis deger girdiniz.");
        }


        return 0;
    }