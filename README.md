
https://colab.research.google.com/drive/1kKgZ9_MdfNQnFyu382_AmzoIWynI4EKE?usp=sharing
Sunum Videosu:https://drive.google.com/file/d/1zm5KyGP3QSdrdtozHXZPa31UmIX27O87/view?usp=drive_link

🏠 California Ev Fiyatı Tahmin Sistemi
Bu proje, California'daki konut fiyatlarını tahmin etmek için gelişmiş bir derin öğrenme modeli ve kullanıcı dostu bir etkileşimli arayüz sunar.

📋 Özellikler
🧠 Gelişmiş Derin Öğrenme Modeli: 5 katmanlı sinir ağı mimarisi

📊 Etkileşimli Arayüz: Gerçek zamanlı fiyat tahmini ve analiz

💰 Kira Getirisi Hesaplama: Yatırım değerlendirmesi için kira getirisi analizi

📈 Görsel Karşılaştırmalar: Tahminlerin gerçek değerlerle karşılaştırılması

⚙️ Merkezi Hiperparametre Yönetimi: Tüm ayarlar tek bir yerde

🛠️ Kurulum
Gerekli bağımlılıkları yükleyin:

bash
pip install tensorflow scikit-learn joblib matplotlib pandas numpy ipywidgets
Dosyayı çalıştırın:

bash
python colab_runner.py
🚀 Kullanım
Tam Sistem Çalıştırma
python
run_complete_system()
Bu komut:

Gerekli paketleri kontrol eder

Model dosyalarının varlığını kontrol eder

Gerekirse modeli eğitir

Etkileşimli arayüzü başlatır

Hızlı Model Eğitimi
python
metrics = quick_train()
Modeli hızlıca eğitir ve performans metriklerini döndürür.

Hızlı Tahmin Arayüzü
python
quick_predict()
Önceden eğitilmiş modelle etkileşimli arayüzü başlatır.

🧩 Arayüz Özellikleri
Özellik Ayarları
Medyan Gelir (MedInc): 0.1 - 15.0

Ev Yaşı (HouseAge): 1.0 - 50.0 yıl

Ort. Oda Sayısı (AveRooms): 1.0 - 10.0

Ort. Yatak Odası (AveBedrms): 0.5 - 5.0

Nüfus (Population): 100.0 - 10000.0

Ort. İkamet Eden (AveOccup): 1.0 - 10.0

Enlem (Latitude): 32.0 - 42.0

Boylam (Longitude): -125.0 - -114.0

Analiz Butonları
🔮 Fiyat Tahmini Yap: Seçilen özelliklere göre ev fiyatı tahmini

💰 Kira Getirisi Hesapla: Aylık kira geliri ve yıllık getiri oranı

📊 Gerçek-Tahmin Karşılaştır: Model performansını gerçek verilerle karşılaştırma

Filtreleme Seçenekleri
Fiyat Aralığı: 50K - 1000K $

Karşılaştırma Ev Sayısı: 1-20

Kira Oranı: %30-%150

Model Özellikleri
Optimizer: Adam (Öğrenme Oranı: 0.0006)

Kayıp Fonksiyonu: MSE (Ortalama Karesel Hata)

Regularizasyon: Dropout ve Batch Normalization

Callback'ler: Erken Durdurma, Öğrenme Oranı Azaltma, Model Kaydetme

📊 Performans Metrikleri
Model değerlendirmesi aşağıdaki metriklerle yapılır:

MSE (Mean Squared Error)

RMSE (Root Mean Squared Error)

R² (R-squared)

MAE (Mean Absolute Error)

MAPE (Mean Absolute Percentage Error)

📂 Dosya Yapısı
Eğitim sonrasında oluşturulan dosyalar:

house_price_model.keras: Eğitilmiş model

scaler_X.pkl: Özellik scaler'ı

scaler_y.pkl: Hedef değişken scaler'ı

feature_names.pkl: Özellik isimleri

data_stats.pkl: Veri istatistikleri

X_test.pkl: Test özellikleri

y_test.pkl: Test hedef değişkenleri

original_y_test.pkl: Orijinal test hedef değişkenleri

🌟 Örnek Çıktılar
Fiyat Tahmini:

🏠 Seçilen Ev Tahmini Fiyatı: $350,000
📍 Konum: Enlem 34.0, Boylam -118.0
🔻 Min Fiyat Filtresi: $100,000
🔺 Maks Fiyat Filtresi: $400,000
ℹ️ Grafikte 10 örnek ev ile karşılaştırma yapılmıştır
Kira Getirisi:

🏠 Ev Fiyatı: $350,000
🏡 Aylık Kira: $2,450
📈 Yıllık Getiri: %8.40

data_stats.pkl: Veri istatistikleri

X_test.pkl ve y_test.pkl: Test verileri

