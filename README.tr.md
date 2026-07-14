<div align="center">

# 🌐 Enterprise ERP & CRM Management System
### Modern, Şık ve Tam Kapsamlı Kurumsal Yönetim Platformu

[![Laravel](https://img.shields.io/badge/Laravel_13-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)](https://laravel.com)
[![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Inertia.js](https://img.shields.io/badge/Inertia.js_v3-9553E9?style=for-the-badge&logo=inertia&logoColor=white)](https://inertiajs.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_v4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

<div style="margin-top: 15px; margin-bottom: 15px;">
  <a href="README.md"><img src="https://img.shields.io/badge/Language-English-blue?style=for-the-badge" alt="English"></a>
  <a href="README.tr.md"><img src="https://img.shields.io/badge/Dil-T%C3%BCrk%C3%A7e-e11d48?style=for-the-badge" alt="Türkçe"></a>
</div>

<p align="center">
  <b>Geleneksel SSR (Blade) sınırlarını aşan, Tek Sayfa Uygulaması (SPA) hızında, zengin ve dinamik arayüzlü yeni nesil Kurumsal Kaynak Planlama (ERP) ve Müşteri İlişkileri Yönetimi (CRM) sistemi.</b>
</p>

</div>

---

## 🏗️ Mimari Felsefe: Neden Blade Yerine React + Inertia.js?

Geleneksel Laravel projelerinde her sayfa için ayrı bir `.blade.php` dosyası (SSR) kullanılır ve sayfa geçişlerinde tarayıcı tüm HTML'i baştan yükler (Full Page Reload). 

Bu projede ise **Modern Tek Sayfa Uygulaması (SPA - Single Page Application)** mimarisi benimsenmiştir:
* **Tek Bir Blade Şablonu (`app.blade.php`):** Uygulama yalnızca tek bir HTML giriş kapısına sahiptir. Bu dosya Vite ve React bağlantılarını kurarak tüm kontrolü frontend'e devreder.
* **Tamamen React 19 (`.tsx` / TypeScript) Arayüzü:** Tüm formlar, dinamik tablolar, modallar, Kanban panoları ve sekmeler `resources/js/pages/` altında güçlü React bileşenleri olarak geliştirilmiştir.
* **Inertia.js Köprüsü:** Karmaşık REST API veya GraphQL endpoint'leri oluşturmadan, Laravel Controller'larından doğrudan `Inertia::render()` ile React bileşenlerine veri aktarılır. Bu sayede **backend'de Laravel'in gücü ve güvenliği**, **frontend'de ise React'in eşsiz arayüz akıcılığı** bir araya getirilmiştir.

---

## 🌟 Öne Çıkan Özellikler ve Modüller

### 1. 📊 CRM & Satış Boru Hattı (Sales Pipeline)
* **360° Müşteri & Şirket Yönetimi:** Gelişmiş arama, VIP/Aktif/Lead segmentasyonu ve hızlı müşteri profili modalları.
* **İnteraktif Kanban Boru Hattı:** 5 Aşamalı (Yeni Fırsat ➔ Teklif ➔ Müzakere ➔ Kazanıldı / Kaybedildi) satış sürükle-bırak panosu.
* **Teklif & Etkileşim Takibi:** Profesyonel PDF teklif taslakları ve müşteriyle yapılan toplantı/telefon görüşmelerinin kayıt altına alındığı zaman çizelgesi (*Timeline*).

### 2. 📦 Stok & Depo Yönetimi (Inventory & Warehouses)
* **Kritik Stok Uyarı Sistemi:** SKU ve barkod bazlı ürün kataloğu; stok seviyesi belirlenen eşiğin altına düştüğünde otomatik görsel uyarılar.
* **Çoklu Depo Kartları:** Merkez, şube ve yedek depolar bazında varlık ve miktar takibi.
* **Stok Hareket Fişleri:** Mal Giriş, Mal Çıkış, Depolar Arası Transfer, Fire/Zayiat fişleri ve Tedarikçi Satın Alma Siparişleri (*Purchase Orders*).

### 3. 💰 Finans & Ön Muhasebe (Finance & Accounting)
* **e-Fatura Uyumlu Faturalama:** Satış ve alış faturaları, vade tarihleri takibi ve durum (Ödendi/Bekliyor/Gecikti) filtrelemesi.
* **Cari Hesap Bakiye İzleme:** Müşteri ve tedarikçi net alacak/verecek bakiyelerinin tek ekranda konsolidasyonu.
* **Kasa, Banka ve Giderler:** Tahsilat ve tediye makbuzlarıyla otomatik banka/kasa bakiye senkronizasyonu ve departman masraf takibi.

### 4. 👥 İnsan Kaynakları & Personel (HRM)
* **Personel Özlük ve Departman Kartları:** Kadro KPI'ları, toplam bordro bütçesi ve detaylı çalışan profilleri.
* **Yönetici Onaylı İzin Yönetimi:** Yıllık ve sağlık izinleri için **Onayla / Reddet** iş akışı ve personelin `on_leave` statüsüne otomatik senkronizasyonu.
* **Performans & Prim Takibi:** Çalışan KPI hedeflerinin ve prim ilerleme oranlarının görsel barlarla takibi.

### 5. 🚀 Projeler & Operasyon Panosu (Projects & Tasks)
* **CRM Entegreli Projeler:** Satış anlaşmalarından doğrudan projelere dönüşüm, bütçe ve yedi adımda ilerleme takibi.
* **4 Aşamalı Görev Kanbanı:** `To Do`, `In Progress`, `Review` ve `Done` sütunlarıyla ekip içi görev dağılımı.

### 6. 🛡️ Gelişmiş Güvenlik, RBAC & Denetim Logları
* **İnteraktif İzin Matrisi (RBAC):** Süper Yönetici, Satış Müdürü, CFO, Depo Sorumlusu gibi 6 rol için modül bazlı (Read/Create/Update/Delete) yetkilendirme.
* **Sistem Denetim Logları (*Audit Logs*):** Kullanıcıların sistemde yaptığı tüm ekleme, silme ve güncelleme işlemlerinin IP adresi ve zaman damgasıyla kayda alınması.

### 7. 🎨 Kurumsal Çift Sütunlu Arayüz (Split Sidebar UI)
* **Göz Yormayan Dark / Light Mode:** Sistem tercihine duyarlı anlık tema değiştirme ve oklch renk paleti.
* **İkili Yan Menü Navigasyonu:** Sol tarafta ana ikon menüsü (`SidebarPrimary`), yanında aktif modüle göre dinamik açılan alt menü (`SidebarSecondary`).

### 8. 🌍 Dinamik Çift Dil (TR / EN) & Passkey Kimlik Doğrulama
* **Tam Kapsamlı Çoklu Dil (i18n):** Hem React frontend katmanında (`resources/js/locales/*.ts`) hem de Laravel backend katmanında (`lang/*/*.php`) anlık Türkçe ve İngilizce dil geçişi.
* **WebAuthn Passkey:** Şifresiz ve biyometrik (parmak izi / yüz tanıma / güvenlik anahtarı) güvenli giriş entegrasyonu.

### 9. 🚀 cPanel FTP Otomatik Canlıya Alma (GitHub Actions CI/CD)
* **Bulut Derleme & Dağıtım:** Her `main` push işleminde `.github/workflows/cpanel-deploy.yml` devreye girerek Node.js 20 ile React/Vite bundle'ını derler ve gereksiz dosyaları temizleyerek doğrudan cPanel FTP sunucusuna aktarır.
* **Akıllı Koruma Kalkanı:** Canlı sunucudaki `database.sqlite` ve `.env` dosyaları deployment esnasında korunur, veriler asla ezilmez.

---

## 📂 Proje Klasör Yapısı

```bash
erp-crm-app/
├── app/
│   ├── Http/Controllers/       # CRM, Inventory, Finance, HR, Project, System Controllers
│   └── Models/                 # Eloquent ORM modelleri ve ilişkiler
├── database/
│   ├── migrations/             # Tüm modüllerin ilişkisel veritabanı şemaları
│   └── seeders/                # Test ve demo verileri (Seeder'lar)
├── resources/
│   ├── css/app.css             # Tailwind CSS v4 ve özel stil tanımları
│   ├── views/app.blade.php     # Projenin TEK Blade şablonu (Giriş Taşıyıcısı)
│   └── js/
│       ├── app.tsx             # React & Inertia giriş noktası
│       ├── layouts/            # MainLayout, Header, SidebarPrimary, SidebarSecondary
│       ├── components/         # Yeniden kullanılabilir UI bileşenleri (Modallar, Butonlar, Tablolar)
│       ├── types/              # TypeScript arayüz ve tip tanımlamaları (models.d.ts)
│       └── pages/              # Modül sayfaları (Dashboard, Crm, Inventory, Finance, Hr, Projects, Settings)
├── routes/
│   └── web.php                 # Inertia rotaları ve modül yönlendirmeleri
├── artisan                     # Laravel CLI aracı
├── composer.json               # PHP bağımlılıkları
└── package.json                # Node/React bağımlılıkları
```

---

## 🔒 Kaynak Kod & Kurumsal Lisanslama

Bu depo (`Showcase Repository`), kurumsal **ERP & CRM Yönetim Platformumuzun** mimari yapısını, teknoloji yığınını ve canlı demo özelliklerini tanıtmak amacıyla oluşturulmuş halka açık vitrin reposudur.

* **Kapalı Kaynak Güvencesi:** Ticari fikri mülkiyet haklarını ve kurumsal lisanslama standartlarını korumak amacıyla, sistemin arka plan (`Laravel 13`) ve ön yüz (`React 19 / TypeScript`) kaynak kodları yalnızca üst düzey güvenlikli özel (**Private**) depolarda tutulmaktadır.
* **Canlı Demo Deneyimi:** Sistemin sunduğu şimşek hızındaki Tek Sayfa Uygulaması (SPA) performansını ve tüm kurumsal modüllerini hemen şimdi yukarıdaki **Canlı Demo Adresi** üzerinden (`https://erp-crm-demo.enginbasmaya.com.tr/login`) inceleyebilirsiniz.
* **Lisanslama ve Kod Erişim Talepleri:** Kurumsal sunucu kurulumu, beyaz etiket (`white-label`) lisanslama veya özel kod inceleme talepleriniz için lütfen profesyonel iletişim kanalları üzerinden bağlantıya geçiniz.

---

## 🌐 Canlı Sunucu (cPanel / Shared Hosting) Kurulumu & Salt Okunur Demo Modu

Paylaşımlı sunucularda (cPanel, DirectAdmin vb.) SSH erişimi olmadan dahi veritabanını tek tıkla kurabilmeniz ve inceleme yapabilmeniz için özel bir akıllı kurulum rotası (`/setup-database`) ve koruma kalkanı geliştirilmiştir:

* **Canlı Demo Adresi:** `https://erp-crm-demo.enginbasmaya.com.tr/login`
* **Sıfır Ayar Otomatik Kurulum:** Akıllı başlama mekanizması (`AppServiceProvider`) sayesinde uygulama yeni bir sunucuya yüklendiğinde, tarayıcıdan herhangi bir sayfa açıldığı anda tüm veritabanı tabloları ve test verileri arka planda otomatik olarak oluşturulur. Hiçbir manuel kurulum linkine veya terminal komutuna gerek kalmaz.
* **Salt Okunur Demo Kalkanı (`CheckDemoMode` Middleware):** Müşterilerinizin veya ziyaretçilerinizin sistemi incelerken verileri silmesini veya bozmasını engellemek için `CheckDemoMode` kalkanı devrededir. Demo kullanıcısı sistemi %100 özgürce gezebilir ancak hiçbir ekleme, silme veya değişiklik yapamaz.

### 🛡️ Müşteri İnceleme (Demo) Giriş Bilgileri:
* **E-posta:** `demo@erp.test`
* **Şifre:** `demo123`
*(Giriş yapıldığında sistem otomatik olarak Salt Okunur Demo kilitlerini devreye alır.)*

---

## 🛠️ Katkıda Bulunma (Contributing) & Lisans

Bu proje **MIT Lisansı** altında açık kaynak olarak dağıtılmaktadır. Katkıda bulunmak, hata bildirmek veya yeni modül önerisi sunmak için lütfen `Pull Request (PR)` oluşturun veya bir `Issue` açın.

<div align="center">
  <p><b>✨ Modern Web Teknolojileri ile Geliştirilmiştir ✨</b></p>
</div>
