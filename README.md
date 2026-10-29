# Anadolu 1280 — Taht ve Toprak

**v0.4.3 — Devlet Yolları ve Geniş Defterler**

Oyna: https://kaan12290.github.io/anadolu-1280/

69 şehir bölgesi, 20 oynanabilir ülke ve Ocak 1280 başlangıcı. Harita, şehir konumları ve mevcut parşömen tasarımı korunur. İnternet olmadan `index.html` açılarak oynanabilir.

## Görevler ve büyük ekran

**Devlet → Görev Ağacı** artık geniş ekranda açılır. Selçuklu, Bizans, İlhanlı, Memlük, Bulgar ve Kilikya için toplam 48 devlete özel görev bulunur. Ticaret, sefer ve iç siyaset dallarında şehir, yol, kale, antlaşma ve sadakat şartları açıkça gösterilir. İlk dal ödülü devlet yolunu belirler; diğer dallar kapanır. Tarihten ayrılan sonuçlar “Alternatif hedef” olarak işaretlenir.

Görev ağacı, ikmal/komuta, ticaret ve tarih sayfaları geniş açılır. Başlıktaki **Küçült / Geniş ekran** düğmesiyle boyut değişir. Şehir yönetimi kompakt kalır. Diğer ülkelerin önceki görevleri korunur.

## Yönetim ve kayıtlar

v0.4.2 şehir yöneticileri, aile ağacı, veraset, kültür projeleri ve üst çubuk diplomasi sistemi devam eder. Esir sistemi kapalıdır. Kayıt anahtarı değişmedi; eski seferlerde alınmış görev ödülleri ve seçilmiş dal korunur. Yeni şartlar henüz alınmamış görevlere uygulanır.

## Kaynak ve doğrulama

`anadolu-1280-source.zip` okunabilir kaynak ve testleri; `v0.4.3-history.bundle` Git geçmişini içerir. Kaynak commit'i `SOURCE-COMMIT.txt` içindedir. Kaynakta `npm install`, `npm test`, `npm run build` çalıştırılır; çıktı `dist/index.html` dosyasıdır.

146 otomatik senaryo kontrolü ve tarayıcı doğrulaması geçti. Kapsam ve sınırlamalar `V0.4.3-RELEASE.md`, test özeti `V0.4.3-TESTS.txt` içindedir. Önceki canlı sürüm `backup/v0.4.2-before-missions` dalında korunur.

GitHub Pages kaynağı `main`, `/(root)`, giriş `index.html`. Bu yayın web oyununu günceller; son ayrı Windows paketi v0.4.1'dir.
