# Bilardo projesi notları

Bu dosya, projeye devam ederken bağlamı korumak için. Yeni sohbette Claude’a önce bunu okut.

## Bağlantılar
- Canlı oyun: https://senolgulgonul.github.io/bilardo/
- Repo: https://github.com/senolgulgonul/bilardo
- Yazar: Şenol Gülgönül, "Built with Claude"

## Dosyalar
- `index.html`: İngilizce sürüm, GitHub Pages’te yayında olan
- `bilardo-tr.html`: Aynı oyunun Türkçe sürümü
- `README.md`, `CHANGELOG.md`, `VERSION`: Repo dosyaları
- `extras/`: Başlangıçtaki eğik düzlem (1B) ve eğik masa (2B) simülasyonları

## Sürüm kuralı
- Küçük özellik: 1.1, 1.2… Büyük değişiklik: 2.0
- Her sürümde: CHANGELOG’a madde, VERSION dosyası, sayfa alt bilgisi ve `<meta name="version">` güncellenir
- Zip adı: `bilardo-vX.Y-YYYYMMDD-HHMM.zip` (UTC)

## Fizik motoru (önemli)
- Toplar: konum, hız ve 3B açısal hız (wx, wy, wz). Kayma → yuvarlanma modeli, μ kayma 0.2, yuvarlanma direnci 0.01
- Top–top e = 0.95, bant e = 0.75; bantta yan dönme teğet hızla etkileşir (falso)
- Simülasyon sabit 1 ms adımla çalışır. Yol tahmini aynı motoru önceden koşturur; bu yüzden gerçek atış çizgiyi birebir izler. Adım sistemini değiştirirken determinizmi bozma!
- Güç eğrisi `speedOf()`: alt ve orta güç eskisi gibi (7.35 m/s eğim), en üstte 10 m/s. Atış ve yol tahmini aynı fonksiyonu kullanır
- İnce nişan: düğmeler 0.1°, ok tuşları 0.3°, Shift + ok 0.05°
- Bant modeli (v1.9): bant burnu merkezin üstünde (cepli %63.5 WPA, karambol %60.2 UMB). Tek impuls: normal bileşen eC ile, temas noktasında Coulomb sürtünmesi (μ 0.14, yapışma sınırlı) üç dönme eksenini de etkiler, top zıplamaz. Eski model (sabit 0.6 yapışma, yalnız yan falso) v1.8’de; yavaşlık veya garip davranış olursa geri alınabilir. Ölçüm: yol tahmini ortalama 14 ms → 16 ms
- Modellenmeyenler: squirt, throw, havada sekme, cep çenesi sekmeleri

## Oyun modları
- 8 top (iki oyuncu, gruplar, faul ve ball-in-hand), serbest antrenman (cepli)
- 3 top serbest karambol (hedef 10) ve 3 bant (hedef 5)
- 3 topta resmî kural: Oyuncu 1 beyaz, Oyuncu 2 sarı top; kırmızı ortak hedef

## Şenol’un tercihleri (verilen kararlar)
- Beyazın izi ve "kayıyor/yuvarlanıyor" etiketi kaldırıldı, geri getirme
- Masadaki başlangıç spot noktaları kaldırıldı
- Baş çizgisi (head string) kaldırıldı, geri getirme; açılışta yalnızca gölgeli alan kalsın
- 3 topta "herkes beyazla" seçeneği istenmedi; resmî kural kalsın
- Yol tahmini açık kalsın; "atıştan sonra göster" modu istenmedi
- Yerleşim: masa solda, ekran yüksekliğinin tamamını kullanacak kadar büyük (oran korunur, top büyüklüğü masaya göre gerçek). Sağda 150 px dar sütun, küçük kontroller: başlık + sürüm, skor kartları, dikey güç, 0.1° ince ayar, Vur, Yeni oyun (Vur’un hemen altında), mod, en altta durum mesajı. Diğer her şey aşağıda. Dar ekranda (dikey telefon) alt alta dizilir. Yatay telefonda (yükseklik ≤ 500 px) masaya yakın düzen: sağda 124 px sıkı sütun, başlık gizli, çentik payı var. iOS Safari dikey kaydırıcı çizmediği için orada güç kaydırıcısı `.pwbox` içinde -90° döndürülür (yalnız `@supports (-webkit-touch-callout: none)` + yatay telefon); masaüstünde `.pwbox` display:contents. Yatay telefonda skor kartları grid değil flex (Safari grid’i orada bozuk çiziyordu) (durum mesajı masanın altında)
- Sol paneldeki sürüm etiketi `<meta name="version">`dan otomatik okunur
- Karambolde (3 top ve 3 bant) resmî açılış kuralı: açılış atışı önce kırmızıya vurmalı (UMB), yoksa sayı yok
- 8 topta da resmî WPA kuralı: açılıştan sonra masa açık, grup ilk geçerli sokuşla belirlenir (kafe kuralı istenmedi)
- Yayında yalnızca İngilizce sürüm; dil geçiş bağlantısı şimdilik istenmedi (TR dosyası yine senkron tutulur)
- Sayfa yenilenince her zaman 8 topla açılmalı
- Kısa, sade metinler; LinkedIn’de kapanış "Built with Claude."
