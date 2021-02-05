---
layout: post
title:  "Üçgen eşitsizliği C kodu"
date:   2020-07-23 14:46:09 +0300
categories: problem-solving
---

***SORU :***

Bir üçgende, iki kenarin toplam uzunlugu, üçüncü kenardan az olamaz. Ayrica iki kenarin birbirinden farkının mutlak değeri, üçüncü kenardan büyük olmamalıdır. Bu bilgileri kullanarak, verilen üç kenar uzunluğuna göre bir üçgen çizilip çizilmeyeceğini gösteren programi yazınız. Girilecek kenar uzunluklari tam sayi olacaktır.
                                                                                                                                    
***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        int side1,side2,side3;

        printf("birinci kenari giriniz = ");
        scanf("%d",&side1);

        printf("ikinci kenari giriniz = ");
        scanf("%d",&side2);

        printf("ucuncu kenari giriniz = ");
        scanf("%d",&side3);

        if(side1+side2 < side3||side1+side3 < side2||side2+side3 < side1) 
            printf("Ucgen cizilemez.");

        else printf("Ucgen cizilebilir.");
        return 0;
    }