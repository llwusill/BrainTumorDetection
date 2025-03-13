# Beyin MR Görüntü Sınıflandırma Projesi

## Genel Bakış
Bu proje, beyin MR (manyetik rezonans) görüntülerini iki kategoriye ayırmayı amaçlar: **pozitif** (bir durumu gösteren) ve **negatif** (herhangi bir durum göstermeyen). Veri seti, derin öğrenme (CNN) ve makine öğrenimi teknikleri (SVM ve Naive Bayes) kullanılarak işlenir ve analiz edilir. Proje, Python programlama dili ile TensorFlow, Keras ve Scikit-learn kütüphaneleri kullanılarak geliştirilmiştir.

## Veri Seti
Veri seti, `brain_mri_scan_images` dizininde saklanmaktadır ve iki alt dizin içerir:
- `positive`: Bir durum tespit edilen görüntüler.
- `negative`: Herhangi bir durum tespit edilmeyen görüntüler.

Eğitimden önce veriyi anlamak için örnek görüntüler görselleştirilmiştir.

## Özellikler
- **Veri Ön İşleme**: Görüntüler yüklenir, görselleştirilir ve Keras'ın `ImageDataGenerator` aracıyla eğitime hazırlanır.
- **Konvolüsyonel Sinir Ağı (CNN)**: MR görüntülerini sınıflandırmak için Keras ile bir derin öğrenme modeli oluşturulmuştur.
- **Destek Vektör Makineleri (SVM)**: Scikit-learn'ün SVM modülü ile makine öğrenimi yaklaşımı uygulanmıştır.
- **Naive Bayes**: Gaussian Naive Bayes kullanılarak bir başka makine öğrenimi modeli geliştirilmiştir.
- **Değerlendirme**: Modellerin performansı doğruluk metrikleri ile değerlendirilmiştir.

## Gereksinimler
Bu projeyi çalıştırmak için aşağıdaki kütüphanelerin yüklü olması gerekmektedir:
```bash
pip install numpy pandas matplotlib seaborn tensorflow keras scikit-learn
```

## Proje Yapısı
1️⃣ Veri Hazırlığı: Google Drive bağlama, görüntüleri yükleme ve örnekleri görselleştirme.
2️⃣ CNN Modeli: Keras ile Conv2D, MaxPooling2D ve Dense katmanları kullanılarak oluşturulmuştur.
3️⃣ SVM Modeli: Rastgele oluşturulan verilerle eğitilmiştir (MR özelliklerine uyarlanabilir).
4️⃣ Naive Bayes Modeli: Gaussian Naive Bayes ile sınıflandırma yapılmıştır.
5️⃣ Görselleştirme: Matplotlib ile örnek MR görüntüleri gösterilmiştir.


## Kullanım
1️⃣ Bu depoyu klonlayın
```bash
git clone https://github.com/<kullanıcı-adınız>/<depo-adınız>.git
```
2️⃣ Google Colab'da Drive'ınızı bağlayın (eğer sağlanan not defterini kullanıyorsanız) ve veri setinizin yolunu güncelleyin.
3️⃣Not defterindeki hücreleri adım adım çalıştırarak veriyi işleyin, modelleri eğitin ve sonuçları değerlendirin.


## Sonuçlar
| Model           | Doğruluk                 | Açıklama                              |
|-----------------|--------------------------|---------------------------------------|
| SVM             | ~%98                     | Rastgele örnek veriler üzerinde       |
| Naive Bayes     | ~%94                     | Rastgele örnek veriler üzerinde       |
| CNN             | Değişken                 | Eğitim yapılandırmasına ve veri seti büyüklüğüne bağlı |
