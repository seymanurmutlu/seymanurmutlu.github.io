---
layout: post
title:  "Yüksek Lisans İçin Sıralamaya Dahil Edilebilirliğini Kontrol Eden C Kodu"
date:   2021-02-05 23:58:09 +0300
categories: problem-solving
---

***SORU :***
Lisansüstü eğitim yapmak icin basvuran adayin ALES puanı, yabanci dil puanı ve mezuniyet not ortalamasına göre oluştururan sıralama puanını ile siralamaya girip giremeyecegini ekrana yazdiran programi yaziniz.

Sıralama puanı = ALES sınavının %50'si + Yabanci dil sınavının %25'i + mezuniyet puanının %25'i olarak hesaplanır. Ortalama 60 üzeri ise sıralamaya girebilir.

***ÖRNEK :***    

    ALES puani girin: 80.91
    Yabancidil puani girin: 80.50
    Mezuniyet puani girin: 75.56
                                                                                                                    
    puaniniz: 79.47
    siralamaya girebilir. 
    
***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {  

        float ales,yabancidil,mezuniyet,ort;

        printf("ALES puani girin: ");
        scanf("%f",&ales);

        printf("Yabancidil puani girin: ");
        scanf("%f",&yabancidil);

        printf("Mezuniyet puani girin: ");
        scanf("%f",&mezuniyet);

        ort=ales*0.5+yabancidil*0.25+mezuniyet*0.25;

        printf("----------------------\n");
        printf("puaniniz: %0.2f\n",ort);

        if(ort>=60 && ort<100)
            printf("siralamaya girebilir.");

        if(ort<60 && ort>0)
            printf("siralama giremez.");

        return 0;
    }