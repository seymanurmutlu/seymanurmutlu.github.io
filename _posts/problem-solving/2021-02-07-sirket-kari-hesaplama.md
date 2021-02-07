---
layout: post
title:  "Yatırımlara Göre Şirket Karını Değerlendiren C Kodu"
date:   2021-02-07 11:24:11 +0300
categories: problem-solving
---

***SORU :***

CS101 Holding, üc ayrı alternatif yatırımı değerlendirmektedir. Bu yatırımların başlangıç sermayesi
ve yıllık getirileri belirlenmiştir. Klavyeden girilen sermaye ve her yil sonundaki getiri değerine göre,
(15 yıl sonunda en karlı yatırımın hangisi olduğunu bulup getirilerin sabit olduğu düşünülmelidir.Net kar
bulunurken, toplam getiriden başlangıç sermayesi düşülmelidir.) 

***ÖRNEK :***    

    Birincisin sermayesini ve yillik getirisini girin: 30000 5000

    ikincisinin sermayesini ve yillik getirisini girin: 50000 9000

    Ucuncu sermayesini ve yillik getirisini girin: 70000 10000

    En karli yatirim 2.yatirimdir.     
    

***AÇIKLAMA :***

Üç sermaye değeri, üç sermaye için üç ayrı yıllık getiri değerini tutacağımız değişkenleri tanımlıyoruz.
    
    int birser,biryil,ikiser,ikiyil,ucser,ucyil;

Üç yatırımın net karlarını ayrıca hesaplayıp, bu değerleri tutacak değişkenlerimizi tanımlıyoruz. Soruda, net karlar için 15 yıl sonundaki miktardan sermayeleri düşmemiz gerektiği ibaresi bulunduğu için, ilk başta aldığımız sermaye değerlerini çıkartmayı unutmuyoruz.

    int karbir=15*biryil-birser;
    int kariki=15*ikiyil-ikiser;
    int karuc=15*ucyil-ucser;

Kar değerlerini birbiri ile karşılaştırıyoruz.

    if(karbir>karuc && karbir>kariki) printf("En karli yatirim 1.yatirimdir.");

    if(kariki>karbir && kariki>karuc) printf("En karli yatirim 2.yatirimdir.");

    if(karuc>karbir && karuc>kariki) printf("En karli yatirim 3.yatirimdir.");

***KOD :***

    #include <stdio.h>
    #include <stdlib.h>

    int main()
    {  

    int birser,biryil,ikiser,ikiyil,ucser,ucyil;

        printf("Birincisin sermayesini ve yillik getirisini girin: ");
        scanf("%d %d",&birser,&biryil);
        printf("\n");
        printf("ikincisinin sermayesini ve yillik getirisini girin: ");
        scanf("%d %d",&ikiser,&ikiyil);
        printf("\n");
        printf("Ucuncu sermayesini ve yillik getirisini girin: ");
        scanf("%d %d",&ucser,&ucyil);

        int karbir=15*biryil-birser;
        int kariki=15*ikiyil-ikiser;
        int karuc=15*ucyil-ucser;

        printf("\n");

        if(karbir>karuc && karbir>kariki) printf("En karli yatirim 1.yatirimdir.");

        if(kariki>karbir && kariki>karuc) printf("En karli yatirim 2.yatirimdir.");

        if(karuc>karbir && karuc>kariki) printf("En karli yatirim 3.yatirimdir.");

        printf("\n");
        return 0;
    }