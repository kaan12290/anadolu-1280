# Anadolu 1280 — Taht ve Toprak

**0.3.2 — İtibar ve Nüfuz**

Oyna: https://kaan12290.github.io/anadolu-1280/

## İtibarın yeni işlevi

İtibar 40/60/80/100 düzeylerine çıktığında elçilerin ilişki kazancı artar;
ittifak için gereken ilişki eşiği düşer. İttifakta iki ülkenin yüksek olan
itibar bonusu kullanılır.

- **Elçi heyeti:** 15 itibar; barıştaki bir ülkeyle en çok +25 ilişki; 6 ay bekleme.
- **Divan desteği:** 20 itibar; en çok +8 istikrar, +5 meşruiyet ve +5 saray desteği;
  12 ay bekleme.
- **Muharebe:** zafer +3, yenilgi −2 itibar.
- **Şehir:** fetih +8, şehir kaybı −6 itibar.

Kararlar altın harcamaz. İtibar 0–100 arasında kalır; harcamak diplomatik
bonusları düşürebilir. İtibar sayısına veya Saray Defteri içindeki
İtibar ve Nüfuz kararına tıklayarak pencereyi açabilirsin.

0.3.1 sürümünün saray görselli ana menüsü, haritası ve sefer sistemleri korunur.
Desteklenen eski kayıtlar yeni sürüme aktarılır. Seferler cihazdaki tarayıcıda
saklanır; başka bir siteye ait kayıtlar oyun içinden JSON ile taşınabilir.

## Kaynak ve doğrulama

`anadolu-1280-source.zip` kaynakları, görselleri, harita verilerini ve testleri içerir.
Arşivi açıp kaynak klasöründe `npm install`, `npm test`, `npm run build` çalıştırabilirsin.
57 otomatik kontrol, birleşik uygulama derlemesi ve tarayıcıda karar/kayıt akışı doğrulandı.

## GitHub Pages

Yayın kaynağı `main`, `/(root)`. Giriş dosyası `index.html`; sunucuda derleme gerekmez.
`.nojekyll` doğrudan statik yayın sağlar. Gerekli kod ve görseller HTML içine gömülüdür.
