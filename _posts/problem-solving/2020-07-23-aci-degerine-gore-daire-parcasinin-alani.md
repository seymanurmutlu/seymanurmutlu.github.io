---
layout: post
title:  "Açı değerine göre daire parçasının alanını bulan C kodu"
date:   2020-07-23 14:46:09 +0300
categories: problem-solving
---
***Soru:***
Klavyeden girilen açı değeri ve dairenin yarıçap uzunluğuyla daire parçasının alanı bulun.


    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        int angle;
        float radius,area;
        float PI=3.14;

        printf("Taranacak alanin merkezi angle degerini giriniz = \n");
        scanf("%d",&angle);

        printf("Dairenin yaricap degerini giriniz =  \n");
        scanf("%f",&radius);

        area = PI * radius * radius * (angle/360.0);  
        printf("area = %f",area);

        return 0;
    }
