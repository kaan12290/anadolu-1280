# Anadolu 1280 — Taht ve Toprak

**v0.4.2 — Şehirler ve Hanedanlar**

Oyna: https://kaan12290.github.io/anadolu-1280/

69 şehir bölgesi, 20 oynanabilir ülke ve Ocak 1280 başlangıcı. Mevcut harita ve parşömen arayüzü korunur. İnternet olmadan da `index.html` açılarak oynanabilir.

## Yeni yönetim

Şehri seçip **Şehir yönetimi**ni aç. Her şehrin yöneticisi vardır. Şehir bağlılığı, bey sadakati, hane bütçesi, üst bey ve ferman aynı paneldedir. **Aile ağacı ve evlilik** üzerinden kalıcı kişiler ve varisleri; **Devlet → Hanedan Meclisi** üzerinden talepleri, muhalefeti ve isyanları yönet.

Kültür dönüşümü, hedefi/maliyeti/süresi belli diplomatik güç projesidir. Eski otomatik yüzde kaydırma kaldırıldı. Esir sistemi şimdilik kapalıdır; yaralılar ve iyileşme devam eder. Üst çubuktaki **Diplomasi**, devletler arası ilişki, güven, tehdit ve anlaşmaları gösterir.

Yeni 1280 başlangıcında Sinop ve Kastamonu yerel hanedanları kaynaklıdır. Kişisel adı doğrulanmayan diğer yerel yöneticiler açıkça oyun karakteri olarak belirtilir. Topluluk yüzdeleri tarihî nüfus sayımı değildir.

## Kaynak ve testler

`anadolu-1280-source.zip` okunabilir kod, varlıklar ve testleri; `v0.4.2-history.bundle` geliştirme geçmişini içerir. Kaynak commit `SOURCE-COMMIT.txt` dosyasındadır.

Kaynak klasöründe `npm install`, `npm test`, `npm run build`. Çıktı `dist/index.html`. Ayrıntılı değişiklikler, testler ve kapsam sınırları `V0.4.2-RELEASE.md` / kaynakta `docs/V0.4.2-RELEASE.md` içindedir. Eski sürüm `backup/v0.4.1-before-city-dynasties` dalında korunur.

Kayıtlar cihazda tutulur. Mevcut otomatik kayıt anahtarı korunur; eski seferler yüklemede taşınır. Farklı siteler arasında JSON dışa/içe aktarımı kullanılır. Windows için son ayrı paket v0.4.1'dir; bu yayın web oyununu günceller.

## GitHub Pages

Kaynak `main`, `/(root)`, giriş `index.html`. `.nojekyll` statik yayın sağlar. Kod ve görseller tek HTML dosyasına gömülür.
