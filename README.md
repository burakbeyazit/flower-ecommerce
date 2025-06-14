#  E-Ticaret Çiçek Uygulaması

Modern ve modüler mimariler kullanılarak geliştirilmiş bir çiçek satış platformudur. Kullanıcılar kolayca giriş yapabilir, ürünleri inceleyebilir, sipariş verebilir ve sepetini yönetebilir. Uygulama Domain-Driven Design (DDD) prensipleriyle .NET Core ve Next.js teknolojileriyle inşa edilmiştir.

---



## 👥 Katkıda Bulunanlar

* Burak Beyazıt 170119021
* Sümeyye Naçar 137418009
* Halit Bağcı 170423841

---


## Teknolojiler

### ✅ Backend

* **.NET Core 8** – RESTful API yapısı
* **Domain-Driven Design (DDD)** – katmanlı, modüler mimari
* **PostgreSQL** – ilişkisel veri tabanı
* **Entity Framework Core** – ORM yönetimi

### ✅ Frontend

* **Next.js** – React tabanlı modern frontend yapısı
* **Tailwind CSS** – responsive arayüzler için (opsiyonel)

---

##  Özellikler

* ✅ Kullanıcı kayıt & giriş (Register / Login)
* 🍭️ Ürün listesi & ürün detay sayfaları
* 🛒 Sepet (Cart) yönetimi
* 📦 Sipariş oluşturma ve takip etme (Order)
* 👩‍🌾 Satıcı paneli (opsiyonel)
* 🔄 JWT authentication (token bazlı oturum yönetimi)
* 📂 Katmanlı yapı: `Application`, `Domain`, `Infrastructure`, `Web`

---

##  Proje Mimarisi (Backend - DDD)

```
Flowerify.Backend
│
├— Application      # UseCase’ler ve servisler
├— Domain           # Entity, Aggregate, Value Object, Repository interface
├— Services   # EF Core, dış servis adapterları
└— API           # Controller, DTO, Middleware
```

---

##  Veritabanı

* PostgreSQL kullanıldı.
* Migration yönetimi `dotnet ef` CLI komutları ile yapılır.


##  Frontend Özeti

* Next.js ile SSR destekli e-ticaret arayüzü
* API ile entegre veri çekme (orders, market, login vb.)
* Kullanıcı dostu, mobil uyumlu tasarım
* Authentication token’ları cookie/tabanlı yönetim

---

##  Kurulum

###  PostgreSQL kurulumu

PostgreSQL 15+ versiyonu yüklü olmalıdır. `.env` veya `appsettings.json` dosyasında bağlantı bilgisi girilmelidir.

###  Backend çalıştırma

```bash
cd Flowerify.Backend
dotnet restore
dotnet build
dotnet ef database update
dotnet run --project Flowerify.WebAPI
```

###  Frontend çalıştırma

```bash
cd Flowerify.Frontend
npm install
npm run dev
```

---


##  Lisans

Bu proje MIT lisansı ile lisanslanmıştır.
