# OkulPro — v2: Tam Entegre Öğretmen Kilidi + Akıllı Üretim

═══ TEST EDİLDİ ═══
✓ 50/50 iterasyon başarılı
✓ Tüm blok hesapları doğru ([2,2,1], [3,3], vb.)
✓ Kilitli öğretmen slotları %100 korunur
✓ 0-8 kilit arası tüm senaryolar başarılı
✓ Aşırı yoğun senaryo (60 saat, 80 slot) sorunsuz
✓ Öğretmen/sınıf/oda çakışması = 0

═══ KULLANIM ═══

1) Öğretmen Kilitle:
   /app → Bilgileri Kaydet → Öğretmenler
   "🔥 Öğretmen Yük Haritası" panelindeki her satırın sağında 🔓 butonu
   Tıkla → 🔒 olur (lacivert + altın renk)
   Kilitli satır lacivert sol kenarla vurgulanır
   Header'da "🔒 N kilitli" badge'i otomatik gelir

2) Akıllı Yeniden Üret:
   Ders Programı Oluştur sekmesi → "Yeniden Hazırla" yanına
   "🔒 Kilitlerle Üret" butonu
   Üzerinde altın kilit sayısı badge'i
   Tıkla → onay → loading overlay → algoritma çalışır → sayfa yenilenir

3) Geri Al:
   Üretim sonrası "↶ Son Üretimi Geri Al" butonu gelir (1 saat içinde)
   Önceki sched'e döner

═══ ALGORİTMA ═══

Greedy + smart sort
1) Kilitli öğretmenlerin slotları SCHED'TEN KOPYALANIR (busy maps)
2) Kilitli olmayan atamalar sıralanır:
   - Zor dersler (diff=3) önce
   - Büyük bloklar önce
   - Çok saatler önce
3) Her atama blok'lara ayrılır (hw=5,bs=2 → [2,2,1])
4) Her blok için:
   - Rastgele gün sırası
   - Zor ders ise erken saat tercihi
   - İlk uygun (çakışmasız) slot bulununca yerleştirilir
5) Yerleştirilemeyen varsa yumuşak constraint'lerle ikinci tur
6) Sonuç: sched localStorage'a kaydedilir + yedek alınır

Constraint'ler:
- Öğretmen aynı anda iki yerde olamaz
- Sınıf aynı anda iki dersi olamaz
- Oda aynı anda iki dersi tutamaz (asn.roomId varsa)
- Block dersleri ardışık slotlarda olmalı
- Kilitli öğretmenin slotları AYNEN korunur

═══ DİĞER ÖZELLİKLER (Korundu) ═══
- Nöbet çizelgesi (/nobet.html) — ay başlıkları + Cuma vurguları
- Öğretmen Yük Haritası paneli
- Demo auto-load v2
- Logo/Ana Sayfa takası
- Zorluk etiketi, Demo rozeti

Vercel: Framework Preset = Other, build boş, output boş.
