---
layout: post
title:  "Toplam yakıt maliyetini hesaplayan C kodu"
date:   2020-07-23 14:46:09 +0300
categories: problem-solving
---

***SORU :***

Klavyeden girilen km basina harcanan yakit miktari, yakitin litre fiyati ve aracin yaptigi toplam km miktarina gore aracin toplam yakit maliyetini bulan program yaziniz.

***ÖRNEK :***    
    
    Km basina yakit tuketimi(lt): 0.1
    1 lt yakitin fiyati: 2.080
    Aracin kat ettigi toplam yol: 1000
    -----------------------------------
    Toplam yakit maliyeti: 208 TL
    
***AÇIKLAMA :***

Klavyeden girilen kilometre başına harcanan yakıt miktarı, yakıtın litre fiyatı ve aracın kilometre olarak gittiği yol değerleri için ve hesaplanacak toplam yakıt maliyeti için float değişkenleri tanımlıyoruz.

    float kmFuelConsumption,literPrice,totalDistance,finalCost;

Klavyeden almamız gerekenleri değerleri alıyoruz.

    printf("Km basina yakit tuketimi(lt): ");
    scanf("%f",&kmFuelConsumption);

    printf("\n1 lt yakitin fiyati:");
    scanf("%f",&literPrice);

    printf("\nAracin kat ettigi toplam yol(km): ");
    scanf("%f",&totalDistance);

Maliyeti hesaplayıp yazdırıyoruz.

    finalCost=kmFuelConsumption*literPrice*totalDistance;
    printf("\nToplam yakit maliyeti: %.2f\n",finalCost);

***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {

        float kmFuelConsumption,literPrice,totalDistance,finalCost;

        printf("Km basina yakit tuketimi(lt): ");
        scanf("%f",&kmFuelConsumption);

        printf("\n1 lt yakitin fiyati:");
        scanf("%f",&literPrice);

        printf("\nAracin kat ettigi toplam yol(km): ");
        scanf("%f",&totalDistance);

        finalCost=kmFuelConsumption*literPrice*totalDistance;

        printf("\nToplam yakit maliyeti: %.2f\n",finalCost);

        return 0;
    }