# H3K4me1_H1_human (Задание для индивидуальной работы)

### Анализ пиков гистоновой метки
Выполняем код
```
$ wget https://www.encodeproject.org/files/ENCFF238YJA/@@download/ENCFF238YJA.bed.gz  ENCSR000ANA
$ wget https://www.encodeproject.org/files/ENCFF006PXB/@@download/ENCFF006PXB.bed.gz  ENCSR631RJR


$ zcat ENCFF238YJA.bed.gz  |  cut -f1-5 > H3K4me1_H1.ENCFF238YJA.hg38.bed
$ zcat ENCFF006PXB.bed.gz  |  cut -f1-5 > H3K4me1_H1.ENCFF006PXB.hg38.bed

$ wget https://hgdownload.cse.ucsc.edu/goldenpath/hg38/liftOver/hg38ToHg19.over.chain.gz


$ liftOver   H3K4me1_H1.ENCFF238YJA.hg38.bed   hg38ToHg19.over.chain.gz   H3K4me1_H1.ENCFF238YJA.hg19.bed   H3K4me1_H1.ENCFF238YJA.unmapped.bed
$ liftOver   H3K4me1_H1.ENCFF006PXB.hg38.bed   hg38ToHg19.over.chain.gz   H3K4me1_H1.ENCFF006PXB.hg19.bed   H3K4me1_H1.ENCFF006PXB.unmapped.bed

```
Далее строим графики

* ENCFF006PXB


Отсечка 1500

init            |  Фильтрация
:-------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/54990073/121434365-e6815100-c985-11eb-894b-4f28d369a3e8.png)  |  ![](https://user-images.githubusercontent.com/54990073/121434368-e719e780-c985-11eb-9a73-6ffe78940cb4.png)
* ENCFF238YJA


Отсечка 2000

init            |  Фильтрация
:-------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/54990073/121435450-94412f80-c987-11eb-882e-53b2609c1c42.png)  |  ![](https://user-images.githubusercontent.com/54990073/121435447-93a89900-c987-11eb-8aa4-e8c29cb3591f.png)


ENCFF006PXB          |  ENCFF238YJA
:-------------------------:|:-------------------------:
![](https://user-images.githubusercontent.com/54990073/121440237-3533e880-c990-11eb-80c8-4b78eca25b2b.png)  |  ![](https://user-images.githubusercontent.com/54990073/121440241-35cc7f00-c990-11eb-9b94-ef197acd2196.png)



### Анализ участков вторичной стр-ры ДНК
![len_hist H3K4me1_H1 intersect_with_DeepZ](https://user-images.githubusercontent.com/54990073/121436245-e20a6780-c988-11eb-9afd-3d30bb6374de.png)
### Анализ пересечений гистоновой метки и стр-ры ДНК
![len_hist H3K4me1_H1 merge hg19](https://user-images.githubusercontent.com/54990073/121436246-e2a2fe00-c988-11eb-8c75-259f5adb889b.png)

![graphicschip_seeker H3K4me1_H1 intersect_with_DeepZ plotAnnoPie](https://user-images.githubusercontent.com/54990073/121440672-08340580-c991-11eb-9822-5f77526e214e.png)



### GO 

![image](https://user-images.githubusercontent.com/54990073/121439340-6f9c8600-c98e-11eb-991b-4aa36d3f0a45.png)

