**PROJEDE YER ALANLAR**
--------------------

**Orçun SAATCİ 213405057**

**Pelin YILMAZ 223405003**



**BENZER KİTAPLAR TAHMİNİ** 
------------------------------
* Verilen kitaba benzeyen istenilen sayıda kitabı ve özeti yazdırıyoruz.

* Cosinüs benzerliğinden faydalanıldı


**GEREKLİ İMPORT KODLARI**
--------------------------
from simplemma import text_lemmatizer

import pandas as pd

import numpy as np

import ast

import re

from selenium import webdriver

from selenium.webdriver.chrome.service import Service

from selenium.webdriver.support.wait import WebDriverWait

from selenium.webdriver.support import expected_conditions

from selenium.webdriver.common.by import By

from selenium.common.exceptions import NoSuchElementException



**VERİ SETİNİN OLUŞTURULMASI**
-----------------------------
* Veri setini oluştururken selenium kullandık.
* 1000kitap.com sitesinden veriler çekildi
     - driver.get(f"https://1000kitap.com/kitaplar/en-begenilenler?sayfa={page_num}")
 
* Çekilen veriler txt dosyalarına yazıldı
* 2 adet txt dosyası kullanıldı.
     - books.txt (Kitap adlarının verileri)
     - plots.txt (Kitap özetlerinin verileri)
 
* Toplam 4084 adet kitap adi ve özeti çekildi
* Veriler kitap_adi ve ozet isminde iki kolonu olan bir DataFrame'e aktarıldı.

![Veri Seti](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/a3ceec13-2d9e-4440-b9f9-af8bfbaa6c10)

* Clean_text fonksiyonu metni stop wordslerden temizler

**Temizlenmeden Önce**
![Temizlenmemiş metin](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/ff525f2e-14a4-44e4-a30c-1910f2b3a389)

**Temizlendikten Sonra**
![Temizlenmiş metin](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/1b371ba9-c701-4edb-ab14-16a1af216b4e)

**Clean_text fonkisyonunun DataFrame'e uygulanması**
![updated_df](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/b50799e0-29aa-4420-99a1-3c7e756f7990)


**SÖZLÜK BİLGİSİ**
--------------------
* 4084 kitap adi ve özeti
* 24109 kelime

**TF MATRİSİ**
--------------------
![tf_matrisi](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/071ceaab-07f5-4c5f-b9c4-c75f94a016bf)

**IDF MATRİSİ**
--------------------
![idf_matrisi](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/4bbab77f-9415-4ff7-8136-b21e361b0322)

**TF-IDF MATRİSİ**
--------------------
![tf_idf_matrisi](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/a4113371-05d8-4793-9d0e-204e66a550df)


**TAHMİNLERİN YÜRÜTÜLMESİ**
-------------------------
* benzerleri_bul fonksiyonu istenilen kitaba benzeyen istenilen sayıda kitabı ekrana yazan bir fonksiyondur


**TEST 1**
![test1](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/7a17676e-26cb-4b34-9f9b-b0a20dbdb6a1)


**TEST 2**
![test2](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/ddf6164c-c618-48dc-8bea-59120d53a1a4)

**TEST 3**
![test3](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/d86ba0e3-5731-483d-a4ef-34a156cf2900)

**TEST 4**
![test4](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/c6b1e5c6-f79d-4538-8c3b-eecd15f16de7)

**TEST 5**
![test5](https://github.com/orcunsaatcii/benzer_kitap_tahmini/assets/116540911/d18bdf51-2566-49dd-9a5a-1ddb8f4c444b)







