# Anadolu 1280 — v0.4.4.2 Sade Devlet Yönetimi

Oyna: https://kaan12290.github.io/anadolu-1280/

Hanedan, evlilik, veraset seçimi, yerel bey idaresi ve kişisel iç siyaset şimdilik kapalıdır. Şehirler doğrudan devlete bağlıdır. Tarihî hükümdarlar ve olay akışı, askerî komutanlar, şehir bağlılığı/huzursuzluğu, kültür projeleri, ekonomi, ticaret, savaş ve diplomasi devam eder. Harita ve şehir konumları korunur.

Şehre tıkla → **Şehir yönetimi**. Gelir, insan gücü, bağlılık ve yerel politika aynı defterdedir. **Devlet → Şehirler** şehir listesini; **İkmal ve Komuta** komutanları, merkez yedeğini ve yaralıları gösterir. Görev ağacının eski iç siyaset dalı şehir idaresine uyarlanır; alınmış ödüller tekrar verilmez.

Eski kayıt açılırken bey hazinesi ve mevcut askerleri bir kez devlet hazinesine/merkez yedeğine aktarılır. Eski aile ve siyaset verileri etkin olmayan kayıt olarak korunur. Depolama uygunsa değişmemiş eski JSON ayrıca saklanır; **Kayıt → Güncelleme öncesi kaydı indir** ile alınabilir.

`index.html` dosyasını indirip doğrudan açarak çevrimdışı oynayabilirsin.

Bu depodaki `anadolu-1280-source.zip` önceki **v0.4.4.1 kaynak temelidir**; ikili dosya yükleme aracındaki zaman aşımı nedeniyle bu yayında değiştirilmedi. Güncel okunabilir kaynak değişiklikleri `v0.4.4.2-source.patch` dosyasındadır. ZIP'i açtıktan sonra, içinde `package.json` bulunan klasörde:

GitHub editörünün CRLF satır sonlarını önce LF'ye dönüştür:

```sh
node -e "const fs=require('fs'),p='../v0.4.4.2-source.patch';fs.writeFileSync(p,fs.readFileSync(p,'utf8').replace(/\r\n/g,'\n'))"
git apply --check ../v0.4.4.2-source.patch
git apply ../v0.4.4.2-source.patch
npm install
npm test
npm run build
```

Yama yolunu indirdiğin yere göre düzenle. Çıktı `dist/index.html` olur. Yama, önceki kaynak ZIP'i üzerine harita/görsel dosyalarını değiştirmeden tüm kaynak, kayıt göçü, test ve belge değişikliklerini uygular. Ekran görüntüleri yama dışındadır. Tam bağımsız v0.4.4.2 kaynak ZIP'i ayrıca teslim edilmiştir. Görünen sürüm 0.4.4.2; npm etiketi 0.4.4-state.2'dir.

198 kontrol geçti: 104 güncel oynanış/kayıt kontrolü, 94 arşiv sistem regresyonu. Arşiv testleri yalnız geliştirme seçeneği `legacyManagement:true` ile çalışır; oyunda eski yönetimi açan bir seçenek yoktur. Yeni 25 kontrol, yedi ülkeyle 240 aya kadar seferi de kapsar. Fiziksel telefon testi yapılmadı; 390 × 844 mobil görünüm denetlendi.

Yama uygulandıktan sonraki raporlar: `docs/V0.4.4.2-RELEASE.md`, `docs/checks/v0442-tests.txt` ve ham test çıktısı. Dağıtım deposunda sürüm/test raporları kök dizindedir. Önceki canlı sürüm `backup/v0.4.4.1-before-simple-management` dalında korunur.

Bu güncellemenin kaynak commit'i `de12e479d8fe0022d6509b5109183c374b426aac`tır. Depodaki eski `SOURCE-COMMIT.txt`, `SHA256SUMS.txt` ve history.bundle dosyaları v0.4.4.1 temel paketine aittir; güncel yayın özeti ve oyun dosyası doğrulama değeri `V0.4.4.2-RELEASE.md` içindedir. Ayrı Windows çalıştırılabilir paketi bu kapsamda yenilenmedi.
