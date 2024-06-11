---
title: "Text Extraction Evaluation Metrics: WER, CER, MER, Levensthein Distance"
categories: "NLP"
tags: NLP
---

<style>
    p img {
        margin: auto;
    }
</style>

Untuk mengukur seberapa jauh kualitas model teks ekstraksi entah berupa _speech-to-text_ atau _image-to-text_. Kita dapat menerapkan beberapa _evaluation metrics_ yang sudah umum digunakan: _Levensthein Distance_, _Word Error Rate (WER)_, _Character Error Rate (CER)_, dan _Match Error Rate (MER)_. Tulisan ini merupakan kliping dari eksplorasi yang saya temukan dari beberapa sumber di internet.  

Berhubung saya hanya akan "memasak" data berbentuk teks, maka bahan yang diperlukan hanya 2:  

- teks **_reference_** yang dibuat oleh manusia berperan sebagai _ground truth_; dan 
- teks **_hypothesis_** yaitu hasil ekstraksi oleh _model_. 

Konsep dari _evaluation metrics_ ini dengan mencari seberapa banyak karakter yang berbeda atau salah atau bisa kita sebut _"error"_ antara teks _reference_ dengan teks _hypothesis_. Perbedaan atau _error_ tersebut dapat dibagi menjadi 3 tipe:

1. **Substitution (S):** apabila terdapat **perubahan** karakter/kata pada teks _hypothesis_

2. **Insertion (I):** apabila ditemukan **tambahan** karakter/kata pada teks _hypothesis_

3. **Deletion (D):** apabila terjadi **hilang/berkurangnya** karakter/kata pada teks _hypothesis_

<table border="1" style="width: 80%; margin: 2em auto ;">
    <tr>
        <th></th>
        <th style="text-align: center; ">Substitution</th>
        <th style="text-align: center; "></th>
        <th style="text-align: center; ">Insertion</th>
        <th style="text-align: center; "></th>
        <th style="text-align: center; "></th>
        <th style="text-align: center; "></th>
        <th style="text-align: center; ">Deletion</th>
    </tr>
    <tr>
        <td><b>Reference</b></td>
        <td style="text-align: center; ">Pak</td>
        <td style="text-align: center; ">Budi</td>
        <td style="text-align: center; "></td>
        <td style="text-align: center; ">makan</td>
        <td style="text-align: center; ">bakso</td>
        <td style="text-align: center; ">malang</td>
        <td style="text-align: center; ">enak</td>
    </tr>
    <tr>
        <td><b>Hypothesis</b></td>
        <td style="text-align: center; ">Dek</td>
        <td style="text-align: center; ">Budi</td>
        <td style="text-align: center; ">belum</td>
        <td style="text-align: center; ">makan</td>
        <td style="text-align: center; ">bakso</td>
        <td style="text-align: center; ">malang</td>
        <td style="text-align: center; "></td>
    </tr>
</table>


Pada contoh di atas dapat dilihat terdapat total 3 perubahan pada teks _hypothesis_:

    S: Pak   =>  Dek  
    I:       =>  belum  
    D: enak  =>  

----

## Levensthein Distance
Levensthein distance termasuk ke dalam kategori [edit distance](https://en.wikipedia.org/wiki/Edit_distance) yang merupakan sebuah cara untuk mengetahui perbedaan antara 2 teks/string dengan melihat jumlah perubahan (_edit_) **karakter** yang terjadi.  

![LD=\frac{S+I+D}{n\,%20Karakter\,%20Reference](https://latex.codecogs.com/svg.latex?\Large&space;\color{White}LD=S+I+D) 

Di mana:

    S = Jumlah substitution
    I = Jumlah insertion
    D = Jumlah deletion

Jadi:

    LD = 1 + 1 + 1
    LD = 3

## Character Error Rate (CER)
CER memiliki konsep yang cukup mirip dengan levensthein distance yang sama-sama memanfaatkan karakter sebagai pembanding. Namun, motivasi CER tidak hanya menghitung jumlah perubahan karakter saja, lebih jaun CER menghitung peluang terjadinya perubahan karakter pada teks _hypothesis_ terhadap teks _reference_.

![CER=\frac{S+I+D}{n\,%20Karakter\,%20Reference](https://latex.codecogs.com/svg.latex?\Large&space;\color{White}CER=\frac{S+I+D}{n\,%20Reference}) 

Di mana:

              S = Jumlah substitution
              I = Jumlah insertion
              D = Jumlah deletion
    n Reference = Jumlah karakter dari keseluruhan kalimat

Jadi:

    CER = (1 + 1 + 1) / 32
    CER = 0.09375

## Word Error Rate (WER)
Berbeda dengan metrics sebelumnya yang berfokus pada karakter, WER cenderung melihat dalam jangkauan yang lebar dengan melihat berdasarkan perubahan kata.

![WER=\frac{S+I+D}{n\,%20Karakter\,%20Reference](https://latex.codecogs.com/svg.latex?\Large&space;\color{White}WER=\frac{S+I+D}{n\,%20Reference}) 

Di mana:

              S = Jumlah substitution
              I = Jumlah insertion
              D = Jumlah deletion
    n Reference = Jumlah kata dari keseluruhan kalimat

Jadi:

    WER = (1 + 1 + 1) / 6
    WER = 0.5

## Match Error Rate (MER)
MER merupakan keterbalikan dari WER. MER bertujuan untuk menghitung seberapa banyak kata yang sama atau sesuai dengan teks _reference_.

![MER=\frac{S+I+D}{n\,%20Karakter\,%20Correct](https://latex.codecogs.com/svg.latex?\Large&space;\color{White}MER=\frac{S+I+D}{S+I+D+n\,%20Correct}) 

Di mana:

              S = Jumlah substitution
              I = Jumlah insertion
              D = Jumlah deletion
      n Correct = Jumlah kata benar dari keseluruhan kalimat hypothesis

Jadi:

    MER = (1 + 1 + 1) / (1 + 1 + 1) + 4
    MER = 3 / 3 + 4
    MER = 3 / 7
    MER = 0.428571

----
#### Catatan Kaki: 
Tulisan ini sebagai awal untuk mengenal salah sekian _evaluation metrics_ yang cukup sering ditemui pada pembahasan NLP. Tentu penjelasan di atas terlalu singkat dan mudah, di balik sederhananya konsep di atas terdapat logika matriks dalam melakukan perbandingan antar teks.  

Apabila pembaca hendak mengetahui lebih lanjut saya sudah cantumkan sumber referensi di bawah, yang sekiranya dapat dikunjungi setelah membaca tulisan ini.

----
#### Referensi:

- [WER, CER, and MER](https://docs.kolena.com/metrics/wer-cer-mer/)
- [Deciphering Accuracy: Evaluation Metrics in NLP and OCR- A Comparison of Character Error Rate (CER) and Word Error Rate (WER)](https://medium.com/@tam.tamanna18/deciphering-accuracy-evaluation-metrics-in-nlp-and-ocr-a-comparison-of-character-error-rate-cer-e97e809be0c8)
- [How to calculate the Word Error Rate in Python](https://medium.com/@johnidouglasmarangon/how-to-calculate-the-word-error-rate-in-python-ce0751a46052)
- [Word Error Rate in Python](https://thepythoncode.com/article/calculate-word-error-rate-in-python)
- [Evaluate OCR Output Quality with Character Error Rate (CER) and Word Error Rate (WER)](https://towardsdatascience.com/evaluating-ocr-output-quality-with-character-error-rate-cer-and-word-error-rate-wer-853175297510#bypass)
- [Text Similarity w/ Levenshtein Distance in Python](https://towardsdatascience.com/text-similarity-w-levenshtein-distance-in-python-2f7478986e75)
- [Understanding the Levenshtein Distance Equation for Beginners](https://medium.com/@ethannam/understanding-the-levenshtein-distance-equation-for-beginners-c4285a5604f0)
- [A Beginner’s Guide to the Levenshtein Distance Algorithm (Part 1)](https://javascript.plainenglish.io/a-beginners-guide-to-the-levenshtein-distance-algorithm-part-1-d581fef7588f)