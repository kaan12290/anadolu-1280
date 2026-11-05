# Anadolu 1280 — Taht ve Toprak

**v0.4.5.2 — Şehirler ve Atlas**. Avrupa, Asya ve Kuzey Afrika'da Ocak 1280 başlangıçlı tarihî strateji oyunu.

Canlı oyun: https://kaan12290.github.io/anadolu-1280/

91 görünen siyasi alan ve 315 şehir merkezi. Afrika'da yalnız Mağrip ve Mısır gösterilir; Sahra altı ve Amerika haritada yer almaz. Harita 1300 civarı portolan üslubundan esinlenir; siyasi başlangıç 1280 olarak kalır. Ülke sınırları yaklaşık rekonstrüksiyon, şehir çevreleri oyun tasarımıdır.

Bütün şehir işaretleri her yakınlaştırmada görünür. Yakında şehirler ev, başkentler kale çizimleriyle gösterilir. Şehir adları düğmesi Otomatik / Tümü / Kapalı seçenekleri arasında geçer. Ülke içi yapay bölme çizgileri kaldırıldı. Kesintisiz deniz arka planı ve sınırlı kamera, harita dışındaki köşeli boşlukları önler. Harita sürükleme ve aylık ekonomi hesapları hafifletildi. Mevcut hazine, asker ve kayıtlar korunur. Hanedan, yerel bey ve kişisel iç siyaset yönetimi kapalıdır; ekonomi, ticaret, ordu, diplomasi ve şehir yönetimi sürer.

## Oynama

`index.html` dosyasını indirip tarayıcıda açabilirsin. Uygulama çevrimdışı çalışır. Kayıtlar tarayıcıda saklanır; Kayıt menüsünden JSON olarak indirilebilir. Web adresi ile indirilen dosyanın kayıt alanları ayrıdır.

## Kaynak kod ve doğrulama

`anadolu-1280-source.zip` kaynak kodu, gerekli harita girdilerini, derleme betiklerini ve testleri içerir. `SOURCE-COMMIT.txt` ve `SHA256SUMS.txt` sürüm kaynağını ve dosya özetlerini belirtir. Eski tasarım taslakları dağıtım paketine dahil değildir.

```sh
python -m pip install -r requirements.txt
npm install
python scripts/build-world-map.py
npm run build
npm test
python scripts/check-world-geography.py
```

216 başarılı otomatik kontrol, geometri denetimi ve masaüstü/mobil çerçeve kontrolleri. Fiziksel telefonda FPS veya Windows EXE testi yapılmadı; bu sürüm web ve çevrimdışı HTML güncellemesidir.

## Tarihî kaynaklar

Uyarlanmış Cliopatria / Seshat siyasi verileri CC BY 4.0, Natural Earth fizikî coğrafyası kamu malıdır. Başlangıç yılına göre hanedan ve şehir düzeltmeleri araştırma dosyalarında açıklanır. Moğol halef alanlarında kullanılan 1294 geometrileri 1280'in kesin sınırları olarak sunulmaz. Yeni devletler için ayrıntılı gelecek olay zincirleri bu harita güncellemesinin kapsamında değildir.

Son değişiklikler: `docs/V0.4.5.2-ATLAS.md`. Ayrıntılı atlas kaynakları: `docs/V0.4.5-ATLAS.md`, `source-data/world-research/`, `source-data/CLIOPATRIA-LICENSE.md` ve oyun içi Harita kaynakları.
