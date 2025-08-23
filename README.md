[Google Colab’da Aç](https://colab.research.google.com/gist/denizgcs/1870a1ca46d0795326ff33a75ecff623/miuul_proje_.ipynb)

Kural Tabanlı Sınıflandırma ile 
Potansiyel Müşteri Getirisi Hesaplama
İş Problemi
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 Bir oyun şirketi müşterilerinin bazı özelliklerini kullanarak
 seviye tabanlı (level based) yeni müşteri tanımları (persona)
 İŞ PROBLEMİ
 VERİ SETİ
 DEĞİŞKENLER
 GÖREVLER
 oluşturmak ve bu yeni müşteri tanımlarına göre segmentler
 oluşturup bu segmentlere göre yeni gelebilecek müşterilerin
 şirkete ortalama ne kadar kazandırabileceğini tahmin etmek
 istemektedir.
 Örneğin:
 Türkiye’den IOS kullanıcısı olan 25 yaşındaki bir erkek
 kullanıcının ortalama ne kadar kazandırabileceği belirlenmek
 isteniyor.
MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 Veri Seti Hikayesi
 Persona.csvverisetiuluslararasıbiroyunşirketininsattığıürünlerinfiyatlarınıvebu
 ürünleri satınalankullanıcılarınbazı demografikbilgilerini barındırmaktadır. Veri
 seti her satış işlemindeoluşankayıtlardanmeydanagelmektedir. Bununanlamı
 tablotekilleştirilmemiştir.Diğerbir ifadeilebelirlidemografiközellikleresahipbir
 kullanıcıbirdenfazlaalışverişyapmışolabilir.
 İŞ PROBLEMİ
 VERİ SETİ
 DEĞİŞKENLER
 GÖREVLER
 PRICE SOURCE SEX COUNTRY AGE
 39 android male bra 17
 39 android male bra 17
 49 android male bra 17
 29 android male tur 17
 49 android male tur 17
MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 PRICE –Müşterinin harcama tutarı
 Değişkenler
 SOURCE –Müşterinin bağlandığı cihaz türü
 SEX –Müşterinin cinsiyeti
 COUNTRY –Müşterinin ülkesi
 AGE –Müşterinin yaşı
 persona.csv
 İŞ PROBLEMİ
 VERİ SETİ
 DEĞİŞKENLER
 GÖREVLER
MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 Proje Görevleri
MIUULTM
 Kural Tabanlı Sınıflandırma
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 Uygulama Öncesi Veri Seti :
 PRICE
 39
 39
 49
 29
 49
 SOURCE
 android
 android
 android
 SEX
 male
 COUNTRY
 AGE
 bra
 male
 male
 android
 android
 male
 male
 bra
 bra
 tur
 tur
 17
 17
 17
 17
 17
 Hedeflenen çıktı : 
customers_level_based
 BRA_ANDROID_FEMALE_0_18
 BRA_ANDROID_FEMALE_19_23
 BRA_ANDROID_FEMALE_24_30
 PRICE
 35.6453
 SEGMENT
 B
 34.0773
 33.8639
 BRA_ANDROID_FEMALE_31_40
 BRA_ANDROID_FEMALE_41_66
 34.8983
 36.7371
 C
 C
 B
 A
Görev 1: Aşağıdaki Soruları Yanıtlayınız
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 § Soru 1: persona.csv dosyasını okutunuz ve veri seti ile ilgili genel bilgileri gösteriniz.
 § Soru 2: Kaç uniqueSOURCE vardır? Frekansları nedir?
 § Soru 3:Kaç uniquePRICE vardır?
 § Soru 4:Hangi PRICE'dankaçar tane satış gerçekleşmiş?
 § Soru 5:Hangi ülkeden kaçar tane satış olmuş?
 § Soru 6:Ülkelere göre satışlardan toplam ne kadar kazanılmış?
 § Soru 7:SOURCE türlerine göre satış sayıları nedir?
 § Soru 8:Ülkelere göre PRICE ortalamaları nedir?
 § Soru 9:SOURCE'laragöre PRICE ortalamaları nedir?
 § Soru 10: COUNTRY-SOURCE kırılımındaPRICE ortalamaları nedir?
Görev 2:  COUNTRY, SOURCE, SEX, AGE kırılımında ortalama kazançlar nedir?
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 Elde edilmesi gereken çıktı:
 COUNTRY SOURCE
 0
 1
 2
 3
 4
 bra
 android
 PRICE
 SEX
 female
 AGE
 15
 16
 17
 18
 19
 38.71
 35.94
 35.66
 32.25
 35.20
Görev 3:  Çıktıyı PRICE’a göre sıralayınız.
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 • Önceki sorudaki çıktıyı daha iyi görebilmek için sort_values metodunu azalan olacak şekilde PRICE’a göre uygulayınız.
 • Çıktıyı agg_df olarak kaydediniz. 
Elde edilmesi gereken çıktı:
 COUNTRY SOURCE
 0
 1
 2
 3
 4
 bra
 usa
 fra
 usa
 android
 android
 PRICE
 SEX
 male
 AGE
 46
 male
 android
 ios
 deu
 android
 female
 male
 female
 36
 24
 32
 36
 59.0
 59.0
 59.0
 54.0
 49.0
Görev 4:  Indekste yer alan isimleri değişken ismine çeviriniz.
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 • Üçüncü sorunun çıktısında yer alan PRICE dışındaki tüm değişkenler index isimleridir. Bu isimleri değişken isimlerine çeviriniz.
 İpucu:
Görev 5:  Age değişkenini kategorik değişkene çeviriniz ve agg_df’eekleyiniz.
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 • Age sayısal değişkenini kategorik değişkene çeviriniz.
 • Aralıkları ikna edici şekilde oluşturunuz.
 • Örneğin: ‘0_18', ‘19_23', '24_30', '31_40', '41_70'
 Elde edilmesi gereken örnek çıktı:
 COUNTRY SOURCE
 bra
 usa
 fra
 usa
 android
 android
 android
 SEX
 male
 male
 female
 AGE
 46
 36
 PRICE
 AGE_CAT
 59.0 41_70
 59.0 31_40
 24
 ios
 deu
 android
 male
 female
 32
 59.0
 24_30
 54.0 31_40
 49.0 31_40
 36
Görev 6:  Yeni seviye tabanlı müşterileri (persona) tanımlayınız.
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 • Yeni seviye tabanlı müşterileri (persona) tanımlayınız ve veri setine değişken olarak ekleyiniz.
 • Yeni eklenecek değişkenin adı: customers_level_based
 • Önceki soruda elde edeceğiniz çıktıdaki gözlemleri bir araya getirerek customers_level_baseddeğişkenini oluşturmanız gerekmektedir.
 Bu tabloda bulunan gözlemler bir araya gelecek
 COUNTRY SOURCE SEX
 AGE
 bra
 usa
 fra
 usa
 deu
 android
 android
 male
 male
 android female
 İos
 ios
 male
 female
 46
 36
 24
 32
 36
 Elde edilmesi gereken çıktı
 PRICE
 59.0
 59.0
 59.0
 54.0
 49.0
 AGE_CAT
 41_66
 31_40
 24_30
 31_40
 31_40
 customers_level_based
 BRA_ANDROID_MALE_41_66
 USA_ANDROID_MALE_31_40
 FRA_ANDROID_FEMALE_24_30
 PRICE
 59.0
 59.0
 59.0
 USA_IOS_MALE_31_40
 DEU_ANDROID_FEMALE_31_40
 Dikkat! List comprehension ile customers_level_based değerleri oluşturulduktan sonra bu değerlerin tekilleştirilmesi gerekmektedir.  
Örneğin birden fazla şu ifadeden olabilir: USA_ANDROID_MALE_0_18. Bunları groupby'a alıp price ortalamalarını almak gerekmektedir.
 54.0
 49.0
Görev 7:  Yeni müşterileri (personaları) segmentlere ayırınız.
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 • Yeni müşterileri (Örnek: USA_ANDROID_MALE_0_18) PRICE’a göre 4 segmente ayırınız.
 • Segmentleri SEGMENTisimlendirmesi ile değişken olarak agg_df’e ekleyiniz.
 • Segmentleri betimleyiniz (Segmentlere göre group by yapıp price mean, max, sum’larını alınız).
 İpucu:
Görev 8:  Yeni gelen müşterileri sınıflandırıp, ne kadar gelir getirebileceklerini  tahmin ediniz.
 MIUULTM
 www.miuul.com
 Copyright © Miuul, Inc. All Rights Reserved
 • 33 yaşında ANDROID kullanan bir Türk kadını hangi segmenteaittir ve ortalama ne kadar gelir kazandırması beklenir?
 • 35 yaşında IOS kullanan bir Fransız kadını hangi segmente aittir ve ortalama ne kadar gelir kazandırması beklenir?
 İpucu:
miuul.com
