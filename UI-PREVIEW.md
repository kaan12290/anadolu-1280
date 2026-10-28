# Arayüz taslağı — sade tarihî + harita odaklı

Durum: inceleme için önizleme; canlı GitHub Pages ve Windows 0.4.0 paketi değiştirilmedi.

Kullanıcının seçimi: açık parşömen renkleri, ince üst çubuk, haritanın korunması ve gerektiğinde açılan kenar panelleri. Ek istek: üst çubukta ayrı Diplomasi düğmesi.

## Değişiklikler
- İnce kaynak/tarih çubuğu; Atlas, Saray, Ordular, Tarih, Devlet ve Diplomasi üst gezinmesi.
- Harita tam alanı kullanır. Şehir defteri başlangıçta kapalı; şehir seçilince sağda açılır.
- Şehirde önce gelir, asker katkısı ve huzursuzluk/sadakat özeti. İnşaat, asker toplama, ordu emirleri ve topluluklar açılır bölümlerde.
- Saray, tarih ve devlet defterleri haritanın yanında açılır. Kapatınca haritaya dönülür.
- Günlük yönetim pencereleri haritayı karartmayan, haritadan şehir seçmeye izin veren yan panellerdir. Zorunlu tarihî kararlar, veraset krizleri ve muharebe gibi önemli pencereler mevcut modal davranışını korur.
- Diplomasi düğmesinde gelen teklif sayısı; komşu devletler, ilişki/güven/tehdit özeti; diğer devletler ayrı açılır bölümde.
- Escape ile açık yan panel kapatılır; düğmelerin erişilebilir adları ve mevcut klavye kısayolları korunur.
- Ayrı önizleme otomatik kayıt anahtarı; mevcut kaydı okurken eski anahtar değiştirilmez.

## Kontroller
Derleme başarılı; tüm gömülü JavaScript ayrıştırıldı. Diplomasi ve kayıt göçü 13 kontrol geçti. Tarayıcıda yeni sefer, panel kapatma, üst Diplomasi düğmesi, açık diplomasi penceresinden şehir seçimi, inşaat emri (160 altın bir kez düşer), saray çekmecesi, beyler, ordu yönetimi, aylık rapor ve otomatik kaydı yeniden açma denendi. Oyuna ait konsol hatası gözlenmedi. Simülasyon modülleri, harita verileri ve ana ekran resmi 0.4.0 kaynak commit'i 8baea1a ile aynıdır.

Kaynak: src/game-minimal-ui.css, src/game-minimal-ui.js; derleme ekleri scripts/build-game.mjs; önizleme kayıt anahtarı src/game-app.js. Önizleme canlı sürüme birleştirilmedi. Telefon düzeni CSS ile hazırlandı; gerçek telefonda test edilmedi. Windows paketi bu arayüz taslağıyla yeniden hazırlanmadı.
