---
layout: post
title:  "Kenar Uzunluğu Girilen Karenin Alan ve Çevresini Hesaplayan C Kodu"
date:   2021-02-05 23:58:09 +0300
categories: problem-solving
---

***SORU :***

Klavyeden kenar uzunluğu girilen karenin alanı ve çevresini hesaplayan programı yazın.

***ÖRNEK :***    
    
    Karenin kenarini giriniz =
    1
    Karenin cevresi 4 olarak hesaplanmistir.
    Karenin alani 1 olarak hesaplanmistir.

    
***AÇIKLAMA :***

Değişkenleri tanımlıyoruz.

    float kenar,cevre,alan;

Klavyeden almamız gerekenleri değerleri alıyoruz.

    printf("Karenin kenarini giriniz = \n");
    scanf("%d",&kenar);

Çevre ve alan değerlerini hesaplayıp yazdırıyoruz.

    cevre=4*kenar;
    alan=kenar*kenar;

    printf("Karenin cevresi %d olarak hesaplanmistir.\n",cevre);
    printf("Karenin alani %d olarak hesaplanmistir.\n",alan);

***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        int kenar;
        int cevre;
        int alan;

        printf("Karenin kenarini giriniz = \n");
        scanf("%d",&kenar);

        cevre=4*kenar;
        alan=kenar*kenar;

        printf("Karenin cevresi %d olarak hesaplanmistir.\n",cevre);
        printf("Karenin alani %d olarak hesaplanmistir.\n",alan);
        return 0;
    }