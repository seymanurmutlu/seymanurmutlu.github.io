---
layout: post
title:  "Açı değerine göre daire parçasının alanını bulan C kodu"
date:   2017-09-23 14:46:09 +0300
categories: jekyll update
---
***Soru:***
Klavyeden girilen açı değeri ve dairenin yarıçap uzunluğuyla daire parçasının alanı bulun.


    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {
        int aci;
        float ycap;
        float alan;
        float PI=(3,14);

        printf("Taranacak alanin merkezi aci degerini giriniz = \n");
        scanf("%d",&aci);

        printf("Dairenin yaricap degerini giriniz =  \n");
        scanf("%f",&ycap);

        alan = (float)PI*ycap*ycap*(aci/360);

        printf("alan = %.2f",alan);

        return 0;
    }
