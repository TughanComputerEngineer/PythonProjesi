# PythonProjesi
California Ev Fiyatı Tahmin Sistemi
Bu proje, California'daki konut fiyatlarını tahmin etmek için gelişmiş bir derin öğrenme modeli ve kullanıcı dostu bir etkileşimli arayüz sunar.

Özellikler
🏠 California ev fiyat veri seti üzerinde eğitilmiş derin sinir ağı modeli

📊 Gerçek zamanlı fiyat tahmini ve kira getirisi hesaplama

📈 Model performansını gösteren detaylı görselleştirmeler

🎛️ Özelleştirilebilir hiperparametreler

🔄 Kolay yeniden eğitim ve model kaydetme özelliği

📱 İnteraktif widget'larla kullanıcı dostu arayüz

Kurulum
Gerekli bağımlılıkları yükleyin:

bash
pip install tensorflow scikit-learn joblib matplotlib pandas numpy ipywidgets
Dosyayı çalıştırın:

bash
python colab_runner.py
Kullanım Kılavuzu
Model Eğitimi
python
from colab_runner import quick_train

# Modeli hızlıca eğitin
metrics = quick_train()
Tahmin Arayüzü
python
from colab_runner import quick_predict

# Etkileşimli arayüzü başlatın
quick_predict()
Ana Sistem Çalıştırma
python
from colab_runner import run_complete_system

# Tüm sistemi başlatın (eğitim + arayüz)
run_complete_system()
Etkileşimli Arayüz Özellikleri
Özellik Ayarları:

Medyan Gelir (MedInc)

Ev Yaşı (HouseAge)

Ortalama Oda Sayısı (AveRooms)

Ortalama Yatak Odası (AveBedrms)

Nüfus (Population)

Ortalama İkamet Eden (AveOccup)

Enlem (Latitude)

Boylam (Longitude)

Fonksiyon Butonları:

🔮 Fiyat Tahmini Yap: Seçilen özelliklere göre ev fiyatı tahmini

💰 Kira Getirisi Hesapla: Aylık kira geliri ve yıllık getiri oranı

📊 Gerçek-Tahmin Karşılaştır: Model performansını gerçek verilerle karşılaştırma

Filtreleme Seçenekleri:

Min/Maks Fiyat Aralığı

Karşılaştırma için örnek ev sayısı

Kira oranı yüzdesi

Model Performans Metrikleri
Model değerlendirmesi aşağıdaki metriklerle yapılır:

MSE (Mean Squared Error)

RMSE (Root Mean Squared Error)

R² (R-squared)

MAE (Mean Absolute Error)

MAPE (Mean Absolute Percentage Error)

Hiperparametre Yapılandırması
Tüm hiperparametreler HYPERPARAMS sözlüğünde merkezi olarak yönetilir:

python
HYPERPARAMS = {
    'HIDDEN_LAYERS': [256, 128, 64, 32, 16],
    'DROPOUT_RATES': [0.3, 0.25, 0.2, 0.1, 0.0],
    'EPOCHS': 600,
    'BATCH_SIZE': 32,
    'LEARNING_RATE': 0.0006,
    # ... diğer parametreler
}
Görselleştirmeler
Sistem aşağıdaki görselleştirmeleri sağlar:

Eğitim ve doğrulama kaybı grafikleri

Öğrenme oranı değişim grafiği

Tahmini fiyat karşılaştırma çubuk grafikleri

Kira getirisi ve aylık kira karşılaştırmaları

Gerçek ve tahmini fiyatların karşılaştırılması

Dosya Yapısı
Eğitim sonrasında oluşturulan dosyalar:

house_price_model.keras: Eğitilmiş model

scaler_X.pkl: Özellik scaler'ı

scaler_y.pkl: Hedef değişken scaler'ı

feature_names.pkl: Özellik isimleri

data_stats.pkl: Veri istatistikleri

X_test.pkl ve y_test.pkl: Test verileri

Katkıda Bulunma
Katkılarınız için fork işlemi yapıp pull request gönderebilirsiniz.

