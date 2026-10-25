# Anadolu 1280 — Taht ve Toprak

**0.4.0 — Devlet, Hanedan ve Strateji Güncellemesi**

Oyna: https://kaan12290.github.io/anadolu-1280/

69 şehir bölgesi ve 20 oynanabilir ülkeyle, Ocak 1280'de başlayan tek oyunculu tarihî strateji. Mevcut harita ve ana ekran görseli korunur. İnternet bağlantısı olmadan da tek HTML dosyasından çalışabilir.

## Yeni sistemler
- Şehir ekonomisi ve gelir dökümü; araziye göre birlik avantajları; ordu bölme, birleştirme ve terhis.
- İdari kapasite, yerel beyler, ayrı hazine ve asker yükümlülükleri.
- Şehir bağlılığı, yavaş kültürel değişim, küçük aileler ve karma veraset.
- İç siyaset, önceden işaret veren komutan/bey isyanları; mevcut askerlerin bölünmesi.
- Yaralı, ölü, esir ve firari takibi; fidye, değişim ve esir iadesi.
- Devletler arası ilişki/güven/tehdit; anlaşmalar ve karşı teklifler. Genel itibar göstergesi kaldırıldı.

Yeni paneller **Devlet Yolu** içindedir. **Ordu Yönetimi**, Sefer Masası'ndadır. Şehir politikaları şehir panelinden açılır. Eski canlı otomatik kayıt okunur ve eski anahtarı yedek olarak tutulur. Siteler arasında kayıtlar JSON ile taşınır.

## Kaynaklar ve doğrulama
`anadolu-1280-source.zip` okunabilir kaynak, harita, varlıklar ve testleri içerir. `v0.4.0-history.bundle` yerel geliştirme dalının Git geçmişidir. Kaynak commit `SOURCE-COMMIT.txt` içindedir.

Kaynak klasöründe `npm install`, `npm test`, `npm run build` çalıştırılabilir. Derleme çıktısı `dist/index.html` dosyasıdır. Tarihî itibar testleri kaynakta korunur; kaldırılan mekanik yerine diplomasi regresyonları çalıştırılır.

Ayrıntılı sürüm notları ve test raporu `V0.4.0-RELEASE.md` içindedir. Eski sürüm `backup/v0.3.2-before-v0.4.0` dalında korunur. Windows paketi bu sürüm için yeniden üretilmedi.

## GitHub Pages
Yayın kaynağı `main`, `/(root)`; giriş `index.html`. `.nojekyll` statik yayın sağlar. Kod ve gerekli görseller HTML içine gömülüdür. Kayıtlar kullanıcının tarayıcısında saklanır; sunucuya gönderilmez.
