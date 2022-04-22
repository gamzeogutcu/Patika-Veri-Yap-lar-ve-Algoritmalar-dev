# Insertion Sort Projesi
## [22,27,16,2,18,6] -> Insertion Sort
    
    1. Yukarıda verilen dizinin sort türüne göre aşamalarını yazınız.
    2. Big-O gösterimini yazınız.
    3. Time Complexity: 
    Average case: Aradığımız sayının ortada olması,Worst case: Aradığımız sayının sonda olması, Best case: Aradığımız sayının dizinin en başında olması.
    4. Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.


[7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.

 1. [22,27,16,2,18,6] -> Insertion Sort 

Dizinin o ana kadarki sıralı kısma  ‘ I ‘ koyalım.
* İlk sayıdan bahsettiğimiz için ( 22 ) kendi başına sıralıdır. Hiç bir işlem yapmadan devam eder.

22  I   27  16  2  18  6 
* 27 ile gerisindeki sayı olan 22’yi kıyaslar .27 22den büyüktür. Herhangi bir değişiklik yapılmaz.

22   27  I  16  2  18  6 
* 16 ile bir gerisindeki sayıyı kıyaslar. 16 27den küçüktür. 16 ile 27yi yer değiştirir yani swap yapar. Daha sonra tekrar 16 ile 22yi kıyaslar 16 22den de küçüktür. 16 ile 22yi yer değiştirir.

22   27  I  16  2  18  6 –> 22   16    27 I  2  18  6 –> 16   22    27 I  2  18  6

* 

16   22    27 I  2  18  6 -> 16   22    2   27 I  18  6 -> 16   2    22   27 I  18  6 -> 2   16    22   27 I  18  6

* 

2   16    22   27 I  18  6 -> 2   16    22   18   27 I 6 -> 2   16    18   22   27 I 6 

* 

2   16    18   22   27 I 6 -> 2   16    18   22   6  27 I -> 2   16    18   6   22  27 I -> 2   16    6   18   22  27 I -> 2   6    16   18   22  27 I 
 
 2. Big-O gösterimi\
 1.aşama -> n\
 2.aşama -> n-1\
 3.aşama -> n-2\
         .\
         .\
         .\
         (n-1).aşama -> 2\
         n. aşama    -> 1 tane işlem gerektirir.\
Toplamda
n+(n-1)+(n-2)+...+2+1=[n*(n+1)]/2=0.5n^2+0.5n tane işlem gerektirir.
->O(n^2)






 3. Average case: Aradığımız sayının ortada olması\
 Worst case: Aradığımız sayının sonda olması\
 Best case: Aradığımız sayının dizinin en başında olması
 * 18 avarage case kapsamına girer.

 ## [7,3,5,8,2,9,4,15,6] -> Insertion Sort
* [7 I 3 5 8 2 9 4 15 6] 
* [7 I 3 5 8 2 9 4 15 6] -> [3  7 I 5 8 2 9 4 15 6] 
*  [3  7 I 5 8 2 9 4 15 6] ->  [3  5  7 I 8 2 9 4 15 6] 
* [3  5  7 I 8 2 9 4 15 6] -> [3  5  7  8 I 2 9 4 15 6] 
* [3  5  7  8 I 2 9 4 15 6] -> [3  5  7  2  8 I 9 4 15 6] -> [3  5  2  7  8 I 9 4 15 6] -> [3  2  5  7  8 I 9 4 15 6] -> [2  3  5  7  8 I 9 4 15 6]
* [2  3  5  7  8 I 9 4 15 6] ->  [2  3  5  7  8  9 I 4 15 6]

* [2  3  5  7  8  9 I 4 15 6] -> [2  3  5  7  8  4  9 I 15 6] -> [2  3  5  7  4  8  9 I 15 6] -> [2  3  5  4  7  8  9 I 15 6] -> [2  3  4  5  7  8  9 I 15 6]

* [2  3  4  5  7  8  9 I 15 6] -> [2  3  4  5  7  8  9  15 I 6] 

* [2  3  4  5  7  8  9  15 I 6] -> [2  3  4  5  7  8  9  6  15 I ] -> [2  3  4  5  7  8  6  9  15 I ] -> [2  3  4  5  7  6  8  9  15 I ] -> [2  3  4  5  6  7  8  9  15 I ] 