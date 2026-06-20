# OkulPro — Akıllı Demo Yükleyici v2

DÜZELTME:
- v1 sadece "veri yok" durumunda demo yüklüyordu, eski boş veri kaldıysa atlıyordu
- v2 "veri var ama öğretmen array'i boş" durumunda da demo yükler
- v2 yazdıktan sonra React state'i tazelemek için sayfayı bir kez yeniler 
  (sessionStorage flag ile loop önlenir)
- Console'da detaylı debug log: [OkulPro] Durum: Lisans: VAR/YOK | Veri: BOŞ/DOLU | Demo flag: VAR/YOK

KORUNAN:
- Logo → Tanıtım, Ana Sayfa → Genel Bakış takası
- Sağ alt DEMO rozeti
- Yıldız "ZORLUK:" etiketi
- Yazdırma şablonu sağlam

ÖNEMLİ: Yüklemeden sonra F12 → Application → Clear site data → Ctrl+Shift+R
