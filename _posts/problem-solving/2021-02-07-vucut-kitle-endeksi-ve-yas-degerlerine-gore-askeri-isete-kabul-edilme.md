---
layout: post
title:  "Vucüt Kitle Endeksi ve Yaş Değerlerine Göre Askeri Lisete Kabul Edilme Şartlarını Kontrol Eden C Kodu"
date:   2021-02-07 00:11:09 +0300
categories: problem-solving
---

***SORU :***

Kilo endeksi ve yaş değerlerine göre askeri liseye kabul edilme şartlarını sağlayıp sağlamadığını gösteren bir program yazınız. 13-17 yaşları arasında, 18.50 - 24.99 boy-kilo endeksine sahip olanlar askeri liseye uygun kabul edilir.

***ÖRNEK :***    

    Yasiniz girin: 15
    Kilonuzu girin(kg): 75
    Boyunuzu girin(m): 1.78
    vucut kitle indeksiniz: 23.67
    Tebrikler Askeri liseye girebilirsiniz. 

***AÇIKLAMA :***

Yaş değeri, askeri liseye giriş yaşları arasında değilse vucüt kitle endeksini hesaplamadan programı sonlandırıyoruz. Yaş değeri şartlara uygunsa vucüt kitle endeksini hesaplayarak, şartlara uygunluğunu kontrol ediyoruz.

Burada kullanıdığımız "%.2f" ifadesi, float sayının sadece virgülden sonraki ilk iki basamağını bastırması için kullanılmıştır.

    if(yas>=13 && yas<=17){
        float vki=kilo/(boy*boy); 

        if(vki>=18.50 && vki<=24.99){
            printf("vucut kitle indeksiniz: %.2f \n",vki); 
            printf("Tebrikler Askeri liseye girebilirsiniz.\n");
        }
        else printf("Vucut kitle indeksiniz uygun degildir.");
    }
    else printf("Yasinizdan dolayi okula kabul edilmemektesiniz.");

***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {   

        int yas;
        float boy,kilo;

        printf("Yasiniz girin: ");
        scanf("%d",&yas); //kullanıcının yasını alıyor.
        printf("Kilonuzu girin(kg): ");
        scanf("%f",&kilo); //kullanıcının kilosunu alıyor
        printf("Boyunuzu girin(m): ");
        scanf("%f",&boy); //kullanıcının boyunu alıyor.

        if(yas>=13 && yas<=17){
            float vki=kilo/(boy*boy); //vki=vucut kitle endeksidir ve kilonun boy'un karesine oranıdır.

            if(vki>=18.50 && vki<=24.99){
                printf("vucut kitle indeksiniz: %.2f \n",vki); //%.2f vırgulden sonraki iki basamagi yazdıran float sayi.
                printf("Tebrikler Askeri liseye girebilirsiniz.\n");
            }
            else printf("Vucut kitle indeksiniz uygun degildir.");
        }
        else printf("Yasinizdan dolayi okula kabul edilmemektesiniz.");

        return 0;
    }