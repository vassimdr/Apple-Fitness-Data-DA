# Apple Fitness Veri Analizi Projesi
Bu proje, Apple Fitness uygulaması ile toplanan kişisel sağlık ve aktivite verilerini analiz etmek ve görselleştirmek için Python programlama dili ve Pandas, Plotly gibi kütüphaneleri kullanmaktadır. Projenin amacı, verilerden anlamlı bilgiler çıkarmak, yürüme performansını değerlendirmek ve zaman içindeki değişimleri gözlemlemektir.

# Veri Seti
Veri seti, “Apple-Fitness-Data.csv” adlı bir dosyada saklanmaktadır. Bu dosya, 2022 yılında 30 gün boyunca her dakika kaydedilen 9 farklı metriği içermektedir. Bu metrikler şunlardır:

- Date: Tarih
- Time: Saat
- Step Count: Adım sayısı
- Distance: Kat edilen mesafe (km)
- Energy Burned: Yakılan enerji (kcal)
- Flights Climbed: Tırmanılan kat sayısı
- Walking Double Support Percentage: Yürürken iki ayağın da yere değdiği sürenin yüzdesi
- Walking Speed: Yürüme hızı (km/saat)
- Walking Asymmetry Percentage: Yürürken sağ ve sol bacak arasındaki asimetri yüzdesi
- Veri setinde toplam 43200 satır ve 9 sütun bulunmaktadır. Veri setinde herhangi bir eksik değer bulunmamaktadır.

# Veri Analizi
Veri analizi için Pandas kütüphanesi kullanılmıştır. Pandas, veriyi okumak, temizlemek, işlemek ve manipüle etmek için çeşitli fonksiyonlar sunmaktadır. Veri analizi sürecinde şu adımlar gerçekleştirilmiştir:

- Veriyi okumak için `pd.read_csv()` fonksiyonu kullanılmıştır.
- Verinin ilk beş satırını görüntülemek için `data.head()` fonksiyonu kullanılmıştır.
- Her sütundaki eksik değerlerin sayısını hesaplamak için `data.isnull().sum()` fonksiyonu kullanılmıştır.
- Günlük ortalama adım sayısını hesaplamak için `data.groupby("Date")["Step Count"].mean().reset_index()` fonksiyonu kullanılmıştır.
- Yürüme verimliliğini hesaplamak için `data["Distance"] / data["Step Count"]` formülü kullanılmıştır.
- Zaman aralıklarını hesaplamak için `pd.cut()` fonksiyonu kullanılmıştır.
- Günlük ortalama metrikleri hesaplamak için `data.groupby("Date").mean().reset_index()` fonksiyonu kullanılmıştır.
# Veri Görselleştirme
Veri görselleştirme için Plotly kütüphanesi kullanılmıştır. Plotly, interaktif ve estetik grafikler oluşturmak için çeşitli araçlar sunmaktadır. Veri görselleştirme sürecinde şu adımlar gerçekleştirilmiştir:

- Zaman içinde adım sayısı, kat edilen mesafe, yakılan enerji ve yürüme hızını göstermek için çizgi ve bar grafikleri oluşturmak için `px.line()` ve `px.bar()` fonksiyonları kullanılmıştır.
- Günlük ortalama adım sayısını göstermek için çubuk grafiği oluşturmak için `px.bar()` fonksiyonu kullanılmıştır.
- Zaman aralıklarına göre adım sayısı ve yürüme hızı değişimlerini göstermek için saçılma grafiği oluşturmak için `px.scatter()` fonksiyonu kullanılmıştır.
- Günlük farklı metriklerin ortalamalarını göstermek için treemap grafikleri oluşturmak için `px.treemap()` fonksiyonu kullanılmıştır.
# Sonuç
Bu proje, Apple Fitness uygulaması ile toplanan verileri analiz etmek ve görselleştirmek için Python programlama dili ve Pandas, Plotly gibi kütüphaneleri kullanmıştır. Proje sonucunda, verilerden anlamlı bilgiler çıkarmak, yürüme performansını değerlendirmek ve zaman içindeki değişimleri gözlemlemek mümkün olmuştur.
