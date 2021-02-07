---
layout: post
title:  "Higher-Lower Guessing Game C Kodu"
date:   2021-02-05 23:58:09 +0300
categories: problem-solving
---

***SORU :***

Sizinle higher-lower sayı tahmin oyununu oynayan bir bilgisayar programı oluşturun. Bilgisayar bir sayı seçer ve bilgisayarın seçtiği sayının ne olduğunu tahmin etmeye çalışırsınız. Sizin her tahmininizde bilgisayar, tuttuğu sayının sizin girdiğiniz sayıdan yüksek mi yoksa düşük mü olduğunu söyler. Bilgisayar sizi yönlendirir ve tahmine yaklaştırır.

***ÖRNEK :***    

    Program basladiginda bilgisayarimiz 1 ile 100 arasinda bir sayi tutar.
    Biz klavyeden bir sayi girecegiz ve bilgisayarimiz bizi sayiya dogru yonlendirecek
    Sayiyi kacinci denemende bileceksin?
    Ilk tahmininizi girin : 50

    Yukari Yukari!Yeni tahmin girin :75
                                    
    Asagi Asagi!Yeni tahmin girin :60

    Yukari Yukari!Yeni tahmin girin :65 

    Yukari Yukari!Yeni tahmin girin :70

    Yukari Yukari!Yeni tahmin girin :73

    Kacinci basamakta buldugunu not et ve arkadasinla yaris!

***AÇIKLAMA :***

Rastgele sayı generate etmek için time kütüphanesini kullanıyorum.

    srand(time(NULL)); 

1 ile 100 arasinda herhangi bir sayi atıyorum.

    int sayitut = rand()%100 + 1; 

Klavyeden girdiğimiz sayıların kontrol ve yönlendirmesini yapıyorum.

    while (sayitut != sayi) {
        
        if(sayi<sayitut){
            printf("\nYukari Yukari!");
            printf("Yeni tahmin girin :");
            scanf("%d",&sayi);
        }
            
        else if (sayi>sayitut){
            printf("\nAsagi Asagi!");
            printf("Yeni tahmin girin :");
            scanf("%d",&sayi);
        }
    }


***KOD :***

    #include <stdio.h>
    #include <time.h>
    #include <stdlib.h>

    int main(int argc, const char * argv[]) {
        printf("Program basladiginda bilgisayarimiz 1 ile 100 arasinda bir sayi tutar.\n");
        printf("Biz klavyeden bir sayi girecegiz ve bilgisayarimiz bizi sayiya dogru yonlendirecek\n");
        printf("Sayiyi kacinci denemende bileceksin?\n");
        srand(time(NULL)); 
        
        int sayitut = rand()%100 + 1; //1 ile 100 arasinda herhangi bir sayi ataniyor.
        
        int sayi; //klavyeden alacagimiz sayilar icin;

        printf("Ilk tahmininizi girin : ");
        scanf("%d",&sayi);
        
        
        while (sayitut != sayi) {
            if(sayi<sayitut){
                printf("\nYukari Yukari!");
                printf("Yeni tahmin girin :");
                scanf("%d",&sayi);
            }
            
            else if (sayi>sayitut){
                printf("\nAsagi Asagi!");
                printf("Yeni tahmin girin :");
                scanf("%d",&sayi);
            }
        }
        
        printf("\nKacinci basamakta buldugunu not et ve arkadasinla yaris!\n");

        
        return 0;
    }