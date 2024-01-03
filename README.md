#PROJEDE YER ALANLAR
--------------------
Orçun SAATCİ 213405057
Pelin YILMAZ 223405003



#BENZER KİTAPLAR TAHMİNİ 

Verilen kitaba benzeyen istenilen sayıda kitabı ve özeti yazdırıyoruz.

#GEREKLİ İMPORT KODLARI
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



#VERİ SETİNİN OLUŞTURULMASI
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
