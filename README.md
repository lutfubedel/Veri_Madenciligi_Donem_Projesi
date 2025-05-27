# Veri_Madenciligi_Donem_Projesi

Bu proje, **hava kalitesi sensör verileri** ile bireylerin **duygusal durumları** arasındaki ilişkiyi analiz etmeyi ve bu ilişkiye dayalı olarak **gerçek zamanlı duygu sınıflandırması** yapan bir yapay zekâ modeli geliştirmeyi amaçlamaktadır.

## Projenin Amacı

Hedefimiz, düşük maliyetli taşınabilir sensörler aracılığıyla toplanan **hava kalitesi ölçümleri** (PM, NO₂, CO, NH₃, gürültü seviyesi vb.) ile bireylerin öz bildirim yoluyla ilettiği **duygu durumları** arasında güçlü bir ilişki kurarak, bu verilerden duygusal durumu yüksek doğrulukla tahmin edebilen bir **Random Forest** modeli geliştirmektir.

## Kapsam ve Yaklaşım

- Gerçek dünyadan toplanmış **42.437 örnek içeren veri seti** kullanıldı.
- Veri kümesi, bireylerin bulunduğu çevredeki hava kalitesi değerleri ile aynı anda bildirdikleri 1–5 arası duygusal etiketlerden oluşmaktadır.
- **Random Forest algoritması** kullanılarak sınıflandırma modeli eğitildi.
- Model, edge cihazlar (taşınabilir, çevrimdışı çalışan sistemler) üzerinde çalışacak şekilde tasarlandı.

## Kullanılan Veri Seti

Veriler, **DigitalExposome** isimli önceki bir çalışmadan alınmış olup şu kaynaklardan toplanmıştır:

1. **Enviro-IoT** cihazı: PM1, PM2.5, PM10, NO₂, CO, NH₃, Gürültü (dB)
2. **EnvBodySens mobil uygulaması**: Katılımcılar duygusal durumlarını 1–5 arası puanlayarak bildirmiştir.

### Özellikler (Features):
- IBI, HR, NO2, Noise, NH3, PM10, CO, PM2.5, PM1, EDA, BVP
- Label (1: Çok mutsuz – 5: Çok mutlu)

## 🤖 Kullanılan Algoritma

Model: RandomForestClassifier (Scikit-learn)

**Avantajları:**
- Yüksek doğruluk ve genelleme kabiliyeti
- Aşırı öğrenmeye karşı dirençli
- Düzensiz ve gürültülü çevresel veriler için ideal

## Model Performansı

| Metrik | Değer |
|-------|--------|
| Accuracy | %97 |
| Precision | %95–99 |
| Recall | %95–99 |
| F1-Score | %95–99 |
| AUC | 0.99–1.00 |

- Model, özellikle “çok mutlu” (Label: 5) sınıfında yüksek doğruluk gösterdi.
- Confusion matrix, modelin karışıklık oranının düşük olduğunu gösteriyor.
- ROC eğrileri, sınıflar arası ayrım başarısının yüksek olduğunu doğruladı.

## Sonuçlar

- **Çevresel veriler**, bireylerin ruh halini yüksek doğrulukla tahmin etmede etkili olabilir.
- **Random Forest modeli**, bu tür tahminler için uygun bir çözüm sunmuştur.
- Model, edge cihazlarda çalışacak şekilde optimize edilebilecek düzeyde başarılıdır.
- Çalışma, psikolojik sağlık ve çevresel farkındalık temelli dijital sağlık uygulamalarına temel sağlayabilir.

## Youtube Linki 
 https://youtu.be/q-vq2YO5kOk

