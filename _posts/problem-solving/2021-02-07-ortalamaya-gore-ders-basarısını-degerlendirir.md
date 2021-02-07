---
layout: post
title:  "Ortalamaya Göre Ders Başarısını Değerlendiren C Kodu"
date:   2021-02-07 11:26:11 +0300
categories: problem-solving
---

***SORU :***

Bir dersten alınan vize,final ve devam puanlari girilip, ortalamayı hesapladiktan sonra dersten geçme durumunu ekrana yazdiran c kodunu yazınız.

Ortalama, ortalama puanı = vizenin %40'ı + finalin %50'si + devam puanının %10'u şeklinde hesaplanacaktır. [0-60) puan aralığı başarısız, [60-100] puan aralığı başarılı sayılır. 

***ÖRNEK :***    

    Arasinav notunuzu giriniz =
    90                                                                                                                                      
    Final notunuzu giriniz =
    40                                                                                                                                      
    Devam notunuzu giriniz =
    100

    Agirlikli ortalamaniz = 66.000
    Tebrikler.Gectiniz.  
        
***AÇIKLAMA :***

Vize,final ve devam notlarını tutmak için değişkenleri tanımlıyoruz. Ağırlıklı oratalama değişkenini bize verilen formül kapsamında tanımılıyoruz.

    int arasnv,fnal,devam;
    float aort;

    aort=arasnv*0.40+fnal*0.50+devam*0.10;

Hesaplanmış olan ağırlıklı ortalama değerini, bize verilmiş olan puan aralıkları koşulları ile karşılaştırıyoruz.

    if(aort<60 && aort>0)
        printf("Kaldiniz.\n");

    else if(aort>=60 && aort<=100)
        printf("Tebrikler.Gectiniz.\n");

    else printf("Hatali degerler girdiniz.\n");


***KOD :***

#include <stdio.h>
#include <stdlib.h>

int main()
{

    int arasnv,fnal,devam;
    float aort;

    printf("Arasinav notunuzu giriniz = \n");
    scanf("%d",&arasnv);
    printf("Final notunuzu giriniz = \n");
    scanf("%d",&fnal);
    printf("Devam notunuzu giriniz = \n");
    scanf("%d",&devam);
    printf("-------------------------\n");

    aort=arasnv*0.40+fnal*0.50+devam*0.10;

    printf("Agirlikli ortalamaniz = %.3f \n",aort);
    if(aort<60 && aort>0)
        printf("Kaldiniz.\n");

    else if(aort>=60 && aort<=100)
        printf("Tebrikler.Gectiniz.\n");

    else printf("Hatali degerler girdiniz.\n");

    return 0;

}