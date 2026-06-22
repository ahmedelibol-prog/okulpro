# OkulPro — Buton-Kontrollü Panel Sistemi + Tam Entegre Kilit

YENİ — Bu sürümün değişiklikleri:
- Öğretmenler sekmesinde 2 buton: 🔥 Yük Haritası ve 📅 Gün Haritası
- Her ikisi de varsayılan KAPALI — kullanıcı tıklayınca açılır
- Tercih localStorage'da hatırlanır (okulpro_panels_state)
- Yük Haritası: günlük ders saat dağılımı (ısı haritası)
- Gün Haritası: her öğretmenin müsait/kapalı saatlerini gösteren grid (5 gün × 8 saat)
- Read-only — düzenlemek için Sistem Ayarları > Öğretmen Kısıtları

KORUNDU:
- Tam entegre öğretmen kilidi (🔒) — ana öğretmen listesinde
- Kilitlerle Üret butonu — Ders Programı Oluştur sekmesinde
- Akıllı algoritma: kilitli slotları korur, diğerlerini yeniden dağıtır
- Geri Al sistemi
- Nöbet çizelgesi sayfası
- Demo auto-load, Logo takası, Zorluk etiketi

FLICKER FIX:
- MutationObserver kendi DOM değişikliklerini filtreler (isOurNode)
- Panel'ler dataHash ile idempotent (veri aynıysa rebuild etmez)
- Lock butonları idempotent (state aynıysa dokunmaz)
