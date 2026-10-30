# Bilardo projesi notları

Bu dosya, projeye devam ederken bağlamı korumak için. Yeni sohbette Claude’a önce bunu okut.

## Bağlantılar
- Canlı oyun: https://senolgulgonul.github.io/bilardo/
- Repo: https://github.com/senolgulgonul/bilardo
- Yazar: Şenol Gülgönül, "Built with Claude"

## Dosyalar
- `index.html`: İngilizce sürüm, GitHub Pages’te yayında olan (v1.0)
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
- Modellenmeyenler: squirt, throw, havada sekme, cep çenesi sekmeleri

## Oyun modları
- 8 top (iki oyuncu, gruplar, faul ve ball-in-hand), serbest antrenman (cepli)
- 3 top serbest karambol (hedef 10) ve 3 bant (hedef 5)
- 3 topta resmî kural: Oyuncu 1 beyaz, Oyuncu 2 sarı top; kırmızı ortak hedef

## Şenol’un tercihleri (verilen kararlar)
- Beyazın izi ve "kayıyor/yuvarlanıyor" etiketi kaldırıldı, geri getirme
- Masadaki başlangıç spot noktaları kaldırıldı
- 3 topta "herkes beyazla" seçeneği istenmedi; resmî kural kalsın
- Yol tahmini açık kalsın; "atıştan sonra göster" modu istenmedi
- Güç ve Vur düğmesi masanın hemen altında olmalı
- Kısa, sade metinler; LinkedIn’de kapanış "Built with Claude."
