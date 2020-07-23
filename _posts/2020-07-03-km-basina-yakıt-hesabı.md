---
layout: post
title:  "Toplam yakıt maliyetini hesaplama"
date:   2017-09-23 14:46:09 +0300
categories: jekyll update
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

    float kmyakittuk,litrefiyat,toplamyol,maliyet;

Klavyeden almamız gerekenleri değerleri alıyoruz.

    printf("Km basina yakit tuketimi(lt): ");
    scanf("%f",&kmyakittuk);

    printf("\n1 lt yakitin fiyati:          ");
    scanf("%f",&litrefiyat);

    printf("\nAracin kat ettigi toplam yol: ");
    scanf("%f",&toplamyol);

Maliyeti hesaplayıp yazdırıyoruz.

    maliyet=kmyakittuk*litrefiyat*toplamyol;
    printf("\nToplam yakit maliyeti: %.2f\n",maliyet);

***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {

        float kmyakittuk,litrefiyat,toplamyol,maliyet;

        printf("Km basina yakit tuketimi(lt): ");
        scanf("%f",&kmyakittuk);

        printf("\n1 lt yakitin fiyati:          ");
        scanf("%f",&litrefiyat);

        printf("\nAracin kat ettigi toplam yol: ");
        scanf("%f",&toplamyol);

        maliyet=kmyakittuk*litrefiyat*toplamyol;

        printf("\nToplam yakit maliyeti: %.2f\n",maliyet);

        return 0;
    }