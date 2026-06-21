# OkulPro — Nöbet Çizelgesi Entegrasyonu

YENİ:
- /nobet.html standalone sayfası eklendi
- /app içinde "📋 Nöbet Çizelgesi" butonu (Ana Sayfa yanında)
- Nöbet sayfası OkulPro localStorage'ından öğretmenleri otomatik okur
- Eğer ders programı oluşturulmuşsa: gerçek günlük ders saatleri kullanılır
- Oluşturulmamışsa: atamalardan tahmini saatler (5 güne eşit dağıtım)
- Adil rotasyon algoritması: en az nöbet + bölge çeşitliliği + o gün az dersi olan tercih
- Çıktı: localStorage'a "okulpro_nobet" key'i ile kaydedilir
- Yazdırma desteği

DOSYALAR:
- index.html (mevcut bundle + 4 inject script)
- nobet.html (yeni standalone sayfa)
- Lisans_Yoneticisi.html
- vercel.json, robots.txt, sitemap.xml

Vercel: Framework Preset = Other, build/install/output hepsi boş.
