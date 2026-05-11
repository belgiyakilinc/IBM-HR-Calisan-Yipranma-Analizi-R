# IBM HR Veri Seti ile Çalışan Yıpranması (Employee Attrition) Analizi ve Tahmini

Bu proje, IBM İnsan Kaynakları tarafından toplanan çalışan verileri kullanılarak, "Çalışan Yıpranması" (Employee Attrition - şirketten ayrılma durumu) oranlarını etkileyen faktörleri incelemek ve makine öğrenmesi algoritmalarıyla bu durumu tahmin etmek amacıyla R programlama dili ile hazırlanmıştır.

## 📊 Veri Seti Hakkında
Kullanılan veri seti 1470 gözlemden oluşmakta olup, her bir satır bir çalışanı temsil etmektedir. Çalışanların yıpranma durumlarını (Evet/Hayır) etkileyebilecek demografik, çevresel ve profesyonel değişkenler incelenmiştir:
* **Kişisel Bilgiler:** Yaş, Medeni Hal, Eğitim Seviyesi, Eğitim Dalı
* **İş ve Kariyer Bilgileri:** Departman, Aylık Gelir, Şirkette Çalışılan Yıl, Çalışılan Şirket Sayısı
* **Memnuniyet ve Yaşam Tarzı:** İş Memnuniyeti, Çevre Memnuniyeti, İş-Yaşam Dengesi, Eve Uzaklık

## 🛠 Kullanılan Teknolojiler ve Yöntemler
Proje kapsamında veri manipülasyonu, görselleştirme ve modelleme için temel R kütüphaneleri (`tidyverse`, `ggplot2`, `randomForest`, `caret`) kullanılmıştır. Çalışma üç ana adımdan oluşmaktadır:

1. **Keşifsel Veri Analizi (EDA) ve Görselleştirme:** Çalışanların maaş dağılımları, medeni hal durumları ve memnuniyet seviyeleri ile yıpranma oranları arasındaki ilişkiler yoğunluk (density) grafikleriyle görselleştirilerek analiz edilmiştir.
2. **Makine Öğrenmesi ile Sınıflandırma:** Hedef değişken olan `Yıpranma` durumunu tahmin etmek için eğitim veri seti üzerinde **Random Forest (Rastgele Orman)** algoritması kurularak model eğitilmiştir.
3. **Model Değerlendirme:** Kurulan model test veri seti üzerinde denenmiş, Karmaşıklık Matrisi (Confusion Matrix) hesaplanmış ve sonuçlar görselleştirilmiştir.

## 📈 Öne Çıkan Bulgular ve Model Başarısı
* **Analiz Bulguları:** Çevre ve iş memnuniyeti düşük olan bekar çalışanların yıpranma oranının daha yüksek olduğu; ayrıca düşük gelirli grupta (özellikle AR-GE ve İK departmanlarında) şirketten ayrılma eğiliminin arttığı gözlemlenmiştir.
* **Model Performansı:** Random Forest modeli test verisi üzerinde yaklaşık **%83 doğruluk (Accuracy: 0.829)** skoru elde ederek başarılı bir tahminleme performansı göstermiştir. Hatalı tahminler özel bir matris haritası ile görselleştirilmiştir.

## 🚀 Kullanım
Projede yer alan `.html` veya `.Rmd` uzantılı dosyaları indirerek analizlerin kodlarına ve grafik çıktılarına detaylı olarak ulaşabilirsiniz.
