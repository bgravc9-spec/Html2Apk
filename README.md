# HTML → APK (Android uygulaması)

1. Android Studio (Koala+) ile bu klasörü açın, Gradle 8.7 / JDK 17 kullanın.
2. Cihaza kurun (Run ya da Build > Build APK).
3. Uygulamada: ad + paket adı girin, tek bir .html ya da kökünde index.html olan .zip seçin, "APK oluştur".
4. APK İndirilenler klasörüne kaydedilir; "Yükle" ile kurun (bilinmeyen kaynaklardan yüklemeye izin gerekir).

Nasıl çalışır: uygulama kendi APK'sını şablon olarak kullanır; assets/www içine siteyi koyar,
manifest'teki paket adını ve resources.arsc'teki uygulama adını değiştirir, hizalar ve
apksig ile imzalar. Üretilen APK açılışta assets/www/index.html bulunca WebView'da siteyi gösterir.

Notlar: tüm APK'lar app/src/main/assets/signing.p12 anahtarıyla imzalanır (şifre: html2apk).
Yayın için kendi anahtarınızı koyun. Özel ikon henüz yok.
