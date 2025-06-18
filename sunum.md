# Borsa Tahmin ve Haber Analizi Sistemi - Bitirme Projesi Sunumu

## Açılış (30 saniye)
"Merhaba değerli hocalarımız ve sevgili arkadaşlar. Bugün sizlere 'Borsa Tahmin ve Haber Analizi Sistemi' projemizi sunacağız. Projemiz, yapay zeka ve makine öğrenmesi teknolojilerini kullanarak borsa tahminlerini haber analizleriyle birleştiren yenilikçi bir sistem."

## Sena (5 dakika) - Proje Genel Bakış ve Veri İşleme

"Projemizin temel amacı, yatırımcılara daha doğru tahminler sunabilmek için hisse senedi fiyat verilerini ve haber analizlerini bir araya getiren akıllı bir sistem geliştirmekti.

Sistemimiz iki ana veri kaynağından besleniyor:
1. Yahoo Finance API üzerinden aldığımız gerçek zamanlı borsa verileri
2. Çeşitli haber kaynaklarından topladığımız finansal haberler

Veri işleme sürecimiz üç aşamadan oluşuyor:

İlk olarak, ham borsa verilerimizi Kalman filtresi kullanarak temizliyoruz. Bu filtreleme sayesinde:
- Piyasadaki ani dalgalanmaların etkisini minimize ediyoruz
- Daha stabil ve güvenilir bir veri seti elde ediyoruz

İkinci aşamada, teknik analiz göstergelerini hesaplıyoruz:
- 5 günlük hareketli ortalama (MA5)
- 20 günlük hareketli ortalama (MA20)
Bu göstergeler, trendin yönünü belirlemede kritik rol oynuyor.

Son olarak, tüm bu verileri makine öğrenmesi modellerimiz için uygun formata getiriyoruz.

Şimdi, makine öğrenmesi modellerimizin detayları için sözü Tuğra'ya bırakıyorum."

## Tuğra (5 dakika) - Makine Öğrenmesi Modelleri

"Teşekkürler Sena. Projemizde iki farklı makine öğrenmesi modeli kullanarak ensemble bir yaklaşım geliştirdik.

İlk modelimiz LSTM (Long Short-Term Memory):
- 128 nöronlu ilk katman
- 64 nöronlu ikinci katman
- Dropout katmanları ile overfitting'i önleme
- Sequence length: 20 gün
- Input features: Açılış, Kapanış, En Yüksek, En Düşük fiyatlar ve İşlem Hacmi

İkinci modelimiz Random Forest:
- 400 karar ağacı
- Feature importance analizi sonuçlarına göre:
  * En etkili faktör: Son 5 günlük hareketli ortalama
  * İkinci en etkili: İşlem hacmi
  * Üçüncü en etkili: Haber sentiment skoru

Model performanslarımız:
- LSTM: RMSE değeri 2.34
- Random Forest: RMSE değeri 2.51
- Ensemble (Birleşik): RMSE değeri 2.12

Şimdi, haber analizi sistemimizin detayları için sözü Özgür'e bırakıyorum."

## Özgür (5 dakika) - Haber Analizi ve Duygu Analizi

"Teşekkürler Tuğra. Projemizin en yenilikçi yönlerinden biri, haber analizini fiyat tahminlerine entegre etmemiz.

Haber analizi sistemimiz şu şekilde çalışıyor:
1. Gerçek zamanlı haber toplama
   - Financial Times
   - Reuters
   - Bloomberg gibi güvenilir kaynaklardan

2. Metin Ön İşleme
   - Tokenization
   - Stop-word removal
   - Lemmatization

3. Duygu Analizi
   - BERT tabanlı sentiment analizi
   - -1 (negatif) ile +1 (pozitif) arasında skorlama
   - Haberin yayın zamanına göre ağırlıklandırma

Haber analizinin tahminlere etkisi:
- Pozitif haberler: Ortalama %2.3 yukarı yönlü etki
- Negatif haberler: Ortalama %3.1 aşağı yönlü etki
- Nötr haberler: %0.5'ten az etki

Şimdi, web uygulamamızın detayları için sözü Emir'e bırakıyorum."

## Emir (5 dakika) - Web Uygulaması ve Kullanıcı Arayüzü

"Teşekkürler Özgür. Geliştirdiğimiz tüm bu karmaşık sistemleri kullanıcı dostu bir arayüzle sunmak için Flask tabanlı bir web uygulaması geliştirdik.

Web uygulamamızın özellikleri:
1. Gerçek Zamanlı Analiz
   - Anlık hisse fiyat takibi
   - Canlı haber analizi
   - Dinamik tahmin güncelleme

2. Performans Optimizasyonları
   - Paralel işlem yapısı
   - Önbellek sistemi
   - Asenkron veri güncelleme

3. Kullanıcı Arayüzü
   - Sezgisel tasarım
   - İnteraktif grafikler
   - Mobil uyumlu yapı

4. Teknik Altyapı
   - Python 3.10
   - Flask web framework
   - TensorFlow ve scikit-learn
   - RESTful API mimarisi

## Kapanış ve Gelecek Planları (30 saniye)

Projemizin gelecek dönem hedefleri:
- Kripto para piyasalarına genişleme
- Derin öğrenme modellerinin çeşitlendirilmesi
- Sosyal medya analizi entegrasyonu

Dinlediğiniz için teşekkür ederiz. Sorularınızı yanıtlamaktan memnuniyet duyarız."

## Teknik Demo (Eğer zaman kalırsa)

1. Canlı tahmin gösterimi
2. Haber analizi demo
3. Model performans grafikleri 