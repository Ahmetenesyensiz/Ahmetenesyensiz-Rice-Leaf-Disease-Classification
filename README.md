# Pirinç Yaprağı Hastalıklarının Sınıflandırılması

Bu proje, pirinç yaprak hastalıklarını dört farklı sınıfa (Bacterial Blight, Blast, Brown Spot, Tungro) ayıran bir derin öğrenme uygulamasıdır. Amaç, görsel veriler üzerinden yaprak hastalıklarını yüksek doğrulukla sınıflandırabilen bir sistem geliştirmektir.

## Kullanılan CNN Modelleri

Proje kapsamında dört farklı önceden eğitilmiş model transfer öğrenme yöntemiyle yeniden eğitilmiştir:

- Xception
- VGG16
- MobileNet
- ResNet50

Tüm modeller, ImageNet üzerinde önceden eğitilmiş ağırlıklarla başlatılmış, son katmanları yeniden yapılandırılmış ve pirinç hastalıkları veri kümesi ile eğitilmiştir.

## Veri Kümesi

Veri kümesi dört sınıfa ait görsellerden oluşmaktadır:

- Eğitim verileri: %80
- Test verileri: %20

Her sınıf dengeli sayıda örnek içerecek şekilde dağıtılmıştır. Görseller uygun boyutlara yeniden ölçeklendirilmiş ve veri artırma (augmentation) uygulanmıştır.

## Değerlendirme Metrikleri

Modeller aşağıdaki metriklerle test verisi üzerinde değerlendirilmiştir:

- Accuracy (Doğruluk)
- Precision (Kesinlik)
- Recall (Duyarlılık)
- F1-score

## Sonuçlar

Aşağıda her modelin test verisi üzerindeki performans karşılaştırması sunulmaktadır:

| Model     | Accuracy | Precision | Recall  | F1-Score |
|-----------|----------|-----------|---------|----------|
| Xception  | 0.6083   | 0.6442    | 0.6083  | 0.5864   |
| VGG16     | 0.8711   | 0.8716    | 0.8711  | 0.8700   |
| MobileNet | 0.9949   | 0.9949    | 0.9949  | 0.9949   |
| ResNet50  | 0.8248   | 0.8365    | 0.8248  | 0.8252   |

En iyi performans MobileNet modelinde elde edilmiştir. Eğitim süresi açısından da en hızlı çalışan model MobileNet olmuştur.

## Tahmin Süreleri

Her model için 10 görüntü üzerinden ölçülen tahmin süreleri aşağıda verilmiştir:

| Model     | Tahmin Süresi (10 Görüntü) |
|-----------|-----------------------------|
| Xception  | 3.01 saniye                 |
| VGG16     | 3.49 saniye                 |
| MobileNet | 0.69 saniye                 |
| ResNet50  | 2.26 saniye                 |

## Ekstra Bilgiler

- Eğitimde erken durdurma (EarlyStopping) ve model kontrol (ModelCheckpoint) kullanılmıştır.
- Confusion matrix ve classification report çıktıları `notebooks/` dizininde incelenebilir.
- Model dosyaları `models/` klasöründe kayıtlıdır.

## Gereksinimler

- Python 3.x
- TensorFlow 2.x
- scikit-learn
- matplotlib
- numpy
- pandas

Tüm bağımlılıkları yüklemek için:

pip install -r requirements.txt