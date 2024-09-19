Hisse Senedi Fiyat Tahmini ve Kümeleme Projesi

Bu projede, en yüksek hacimli şirketlerin 2019 yılı için açılış fiyatlarını tahmin eden bir supervised learning (denetimli öğrenme) modeli ve en yüksek hacimli şirketler arasında kümeleme yapan bir unsupervised learning (denetimsiz öğrenme) modeli oluşturulmuştur. İki farklı makine öğrenimi yaklaşımı kullanılarak hisse senedi fiyatlarını analiz etmek amaçlanmıştır. Projeler sırasıyla denetimli ve denetimsiz öğrenme yöntemlerine dayanarak gerçekleştirilmiştir.

1. Proje: Hisse Senedi Fiyat Tahmini (Supervised Learning)
kaggle link : https://www.kaggle.com/code/muhammedyiitzgl/supervisedspk50
Bu projenin amacı, S&P 500 endeksindeki en yüksek hacimli 50 şirketin 2019 yılı açılış fiyatlarını tahmin eden bir model geliştirmektir.

Adım 1: Veri Yükleme ve Keşifsel Veri Analizi (EDA)
Veri Seti: all_stocks_5yr.csv dosyası, S&P 500 endeksinde yer alan şirketlerin 5 yıllık fiyat ve hacim verilerini içermektedir.
İlk olarak veri seti yüklenmiş ve en yüksek hacimli 50 hisse senedi seçilmiştir.
Seçilen hisseler üzerinde çeşitli istatistiksel analizler yapılmış ve eksik veriler temizlenmiştir.
Adım 2: Model Eğitimi
Özellikler (Features): Yüksek, düşük, kapanış fiyatları ve hacim verileri.
Hedef Değişken (Target): Açılış fiyatları.
Model: RandomForestRegressor modeli kullanılarak hisse fiyatları tahmin edilmiştir.
Veri seti eğitim ve test setlerine ayrılmış, veriler StandardScaler ile ölçeklendirilmiştir.
Model, Mean Absolute Error (MAE) ile değerlendirilmiş ve başarılı sonuçlar elde edilmiştir.
Adım 3: 2019 Yılı İçin Tahmin
2019 yılı için her hisse senedinin açılış fiyatı, eğitimli model kullanılarak tahmin edilmiştir.
Tahmin sonuçları, şirket isimlerine göre görselleştirilmiştir.

2. Proje: Hisse Senetlerinin Kümeleme Analizi (Unsupervised Learning)
kaggle link : https://www.kaggle.com/code/muhammedyiitzgl/voltaliteunsupervised
Bu proje, en yüksek hacimli 10 şirketin hisse fiyatlarını kullanarak, şirketlerin benzerliklerine göre kümelenmesini amaçlamaktadır.

Adım 1: Veri Yükleme ve Temizleme
Aynı veri seti kullanılarak en yüksek hacimli 10 hisse senedi seçilmiş ve veri seti ön işleme tabi tutulmuştur.
Eksik veriler temizlenmiş ve yalnızca açılış fiyatı, en yüksek fiyat ve hacim verileri kullanılmıştır.
Adım 2: Kümeleme (K-Means)
K-Means algoritması ile şirketler belirli özelliklerine göre gruplara ayrılmıştır.
Farklı küme sayıları için inertia ve silhouette skorları hesaplanmış ve en uygun küme sayısı belirlenmiştir.
Adım 3: Kümelerin Görselleştirilmesi
Hisse senetleri, açılış fiyatı ve hacim verilerine göre kümelere ayrılarak görselleştirilmiştir.
Projede Kullanılan Kütüphaneler:

pandas: Veri işleme ve analiz.
seaborn, matplotlib: Veri görselleştirme.
scikit-learn: Model eğitimi, kümeleme ve ölçekleme.
Sonuç:

Bu projeler, hem denetimli öğrenme hem de denetimsiz öğrenme yöntemlerinin finansal veri analizinde nasıl kullanılabileceğini göstermektedir. Hisse senedi fiyatlarını tahmin etmek için kullanılan model başarılı bir performans sergilerken, kümeleme analizi ile şirketlerin işlem hacmi ve fiyatlarına göre gruplandırılması sağlanmıştır.

Bu yapı, iki farklı makine öğrenme tekniğini uygulayarak farklı iş problemlerini çözmeye yönelik bir rehber niteliğindedir.
