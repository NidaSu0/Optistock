[README.md](https://github.com/user-attachments/files/29467558/README.md)
<div align="center">

<!-- ANIMATED BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8B5CF6,50:EC4899,100:8B5CF6&height=160&section=header&text=OptiStock&fontSize=52&fontColor=ffffff&fontAlignY=55&animation=twinkling&desc=Stok+%26+CRM+Yönetim+Sistemi&descAlignY=78&descSize=18&descColor=E9D5FF" width="100%"/>

<!-- TYPING ANIMATION -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=8B5CF6&center=true&vCenter=true&width=700&height=60&lines=Ürün+stokunu+takip+et.;Müşterilerini+yönet.;Satışlarını+tek+ekranda+gör.;Yerel+%E2%80%94+hızlı+%E2%80%94+sade.)](https://git.io/typing-svg)

<!-- BADGES -->
![Python](https://img.shields.io/badge/Python-3.8+-8B5CF6?style=for-the-badge&logo=python&logoColor=white)
![Flet](https://img.shields.io/badge/Flet-Flutter_Desktop-EC4899?style=for-the-badge&logo=flutter&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-Yerel_DB-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows_%7C_macOS_%7C_Linux-10B981?style=for-the-badge&logo=windows&logoColor=white)
![License](https://img.shields.io/badge/Lisans-Kişisel_Proje-F59E0B?style=for-the-badge)

</div>

---

## 🧾 Proje Hakkında

**OptiStock**, küçük işletmeler ve kişisel kullanım için geliştirilmiş, tamamen **yerel çalışan** bir stok ve müşteri yönetim masaüstü uygulamasıdır. İnternet bağlantısı gerektirmez, bulut hesabı istemez — tüm veriler makinenizde, sizde kalır.

Flet (Flutter tabanlı) ile yazıldığı için hem Windows'ta hem macOS'ta **aynı görünümde** çalışır. Arayüz tasarımında sadeliği esas aldım; fazla menü, fazla buton yok. Açıyorsunuz, iş yapıyorsunuz.

---

## ✨ Özellikler

| Modül | Ne Yapıyor? |
|:------|:------------|
| 📊 **Dashboard** | Toplam ciro, ürün, müşteri ve sipariş sayısı; son 7 günün çubuk grafiği; son satışlar ve düşük stok uyarıları |
| 📦 **Stok Yönetimi** | Ürün ekleme / listeleme, fiyat ve stok takibi, kategori desteği, renk kodlu stok göstergesi |
| 👥 **CRM** | Müşteri kaydı, e-posta ve telefon bilgisi, kayıt tarihi takibi |
| 🛒 **Satış** | Müşteri + ürün seçerek satış tamamlama, otomatik stok düşme, anlık toplam hesaplama |

---

## 🖥️ Ekran Görüntüleri

> Uygulama ilk açıldığında örnek ürünler, müşteriler ve satış verileriyle birlikte gelir — boş ekranla başlamazsınız.

```
┌─────────────────────────────────────────────────────────┐
│  OS  OptiStock                          Nida Subaşı     │
├──────┬──────────────────────────────────────────────────┤
│      │                                                  │
│ 📊   │   ₺47,837    8 Ürün   6 Müşteri   14 Sipariş   │
│ Dash │                                                  │
│      │   ████ Son 7 Günün Satış Grafiği ████           │
│ 📦   │                                                  │
│ Stok │   Son Satışlar          ⚠ Düşük Stok           │
│      │   Ahmet — RTX 4060      Logitech MX: 2 adet    │
│ 👥   │   Elif — Monitor        WD SSD: 3 adet          │
│ CRM  │                                                  │
│      │                                                  │
│ 🛒   │              by Nida Subaşı | 2026              │
│ Sat. │                                                  │
└──────┴──────────────────────────────────────────────────┘
```

---

## 🚀 Kurulum

### Gereksinimler

- Python 3.8 veya üzeri
- Flet kütüphanesi

### 1. Flet'i Kur

```bash
pip install flet
```

### 2. Repoyu Klonla

```bash
git clone https://github.com/NidaSu0/Optistock.git
cd Optistock
```

### 3. Çalıştır

**Windows:**
```bash
python optistock.py
```
ya da `optistock.py` dosyasına **çift tıkla**.

**macOS / Linux:**
```bash
python3 optistock.py
```

> İlk açılışta `database.db` dosyası otomatik oluşur ve örnek verilerle dolar. Hiçbir kurulum adımı gerekmez.

---

## 📁 Dosya Yapısı

```
Optistock/
│
├── optistock.py                  # Ana uygulama — tüm kod tek dosyada
├── database.db                   # SQLite veritabanı (otomatik oluşur)
└── NASIL_CALISTIRILIR_optistock.txt  # Detaylı kullanım kılavuzu
```

Harici bağımlılık yok, tek `.py` dosyası — indirip çalıştırıyorsunuz.

---

## 🗄️ Veritabanı Şeması

```sql
products   → id | name | price | stock | category | created
customers  → id | name | email | phone | created
sales      → id | customer_id | product_id | quantity | total | date
```

Veriler tamamen yerel — `database.db` dosyasını yedeklemeniz yeterli.

---

## 🛠️ Kullanılan Teknolojiler

```python
{
  "arayuz":     "Flet  (Flutter / Dart motoru, Python API)",
  "veritabani": "SQLite  — standart kütüphane, kurulum yok",
  "dil":        "Python 3",
  "harici_lib": ["flet"]   # tek bağımlılık
}
```

---

## 💡 Neden Flet?

Tkinter ile yeterince vakit geçirdikten sonra bir şeyler denemek istedim. Flet, Python ile Flutter bileşenleri yazmanızı sağlıyor — sonuç gerçekten native görünümlü bir masaüstü uygulaması oluyor. Hem Windows hem macOS'ta aynı `.py` dosyası çalışıyor, platform farkı yazmıyorsunuz.

---

## 📋 Notlar

- Uygulama tamamen **offline** çalışır, veri hiçbir yere gönderilmez
- Stok `≤ 5` olduğunda kırmızı, `≤ 20` olduğunda sarı gösterilir
- Dashboard'daki grafik harici kütüphane kullanmadan sıfırdan yazıldı
- Satış tamamlandığında stok otomatik düşer

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8B5CF6,50:EC4899,100:8B5CF6&height=100&section=footer&animation=twinkling" width="100%"/>

**Nida Subaşı** · 2026 · Üniversite Bitirme Projesi

![Python](https://img.shields.io/badge/Made_with-Python-8B5CF6?style=flat-square&logo=python&logoColor=white)
![Flet](https://img.shields.io/badge/UI-Flet-EC4899?style=flat-square&logo=flutter&logoColor=white)
![SQLite](https://img.shields.io/badge/DB-SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

</div>
