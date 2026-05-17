# 📚 LibPro — Dijital Kütüphane Yönetim Sistemi

![Python Version](https://img.shields.io/badge/Python-3.9+-blue.svg)
![PyQt5](https://img.shields.io/badge/GUI-PyQt5-green.svg)
![SQLite3](https://img.shields.io/badge/Database-SQLite3-lightgrey.svg)
![Matplotlib](https://img.shields.io/badge/Graphics-Matplotlib-orange.svg)
![Architecture](https://img.shields.io/badge/Architecture-MVC--Layered-success.svg)

Modern, dinamik renk temalarına (Koyu Lacivert, Açık Krem vb.) sahip, Python ve PyQt5 kullanılarak geliştirilmiş masaüstü Kütüphane Otomasyon ve Yönetim Sistemi. Nesne Yönelimli Programlama (OOP) ve Katmanlı Mimari (Layered Architecture) prensiplerine uygun olarak temiz, modüler ve sürdürülebilir bir yapıda kodlanmıştır.

## 📸 Ekran Görüntüleri
*(Buraya GitHub'a yüklerken projenin ekran görüntülerini ekleyebilirsiniz)*
## 🌟 Özellikler

### 🛡️ Yetkilendirme ve Rol Yönetimi
* **Rol Tabanlı Erişim:** Admin (Yönetici) ve Üye olmak üzere 2 farklı yetki seviyesi ve bunlara özel dinamik arayüz sekmeleri.
* **Gelişmiş Session:** Başarılı giriş sonrasında kullanıcının oturum bilgileri (kullanıcı adı ve rolü) uygulama genelinde dinamik olarak taşınır.

### ⚙️ Yönetici (Admin) Paneli
* **Kitap Envanter Yönetimi:** Kütüphaneye yeni kitap ekleme, mevcut kitapları listeden tek tıkla silme ve durumlarını (Müsait / Ödünç Verildi) gerçek zamanlı takip etme.
* **Merkezi Süreç Takibi:** Hangi kitabın hangi üye tarafından, hangi tarihler arasında ödünç alındığını gösteren detaylı takip paneli.
* **Gelişmiş Dashboard:** Toplam kitap sayısı, ödünç verilen kitap envanteri ve en popüler/beğenilen kitapların istatistiksel özet kartları (`DashboardCard`).
* **Canlı Veri Analizi:** `Matplotlib` entegrasyonu sayesinde, kütüphanedeki kitapların kategorisel dağılımını dinamik ve gerçek zamanlı bir pasta grafiği (Pie Chart) üzerinde çizme.

### 👥 Üye Paneli
* **Dinamik Kitap Havuzu:** Kütüphanedeki tüm kitapları arama, filtreleme, yazarına ve kategorisine göre anlık inceleme.
* **Ödünç Alma & İade Döngüsü:** Müsait durumdaki kitapları 14 gün süreyle tek tıkla ödünç alma, süresi dolduğunda kolayca kütüphaneye geri teslim etme iş akışı.
* **Favori & Beğeni Sistemi (Toggle):** Kitapları tek tıkla beğenebilme, beğeniyi geri çekebilme ve kişisel favori kitap listesini dinamik olarak görüntüleme.
* **Profil ve Güvenlik Yönetimi:** Mevcut kullanıcı adı ve şifre bilgilerini, veritabanı ilişkisel bütünlüğünü (FOREIGN KEY) koruyarak güvenli bir şekilde güncelleyebilme paneli.

## 🛠️ Mimari ve Teknolojiler

* **Programlama Dili:** Python 3.9+
* **Arayüz (GUI):** `PyQt5` kütüphanesi (`QStackedWidget`, `QTableWidget` ve özel `QFrame` bileşenleri kullanılarak tek pencere üzerinde pürüzsüz sayfa geçişleri sağlanmıştır).
* **Veri Görselleştirme:** `Matplotlib` ve `Numpy` (`FigureCanvasQTAgg` arka yüzü ile Qt GUI içerisine gömülü, arayüz temasıyla uyumlu grafik çizimi).
* **Veritabanı:** SQLite3 (Veriler yerel olarak `libpro.db` içerisinde saklanır, harici bir sunucu kurulumu gerektirmez).
* **Mimari:** GUI (Arayüz), Veritabanı (Data Access) ve İş Mantığı (Domain Models) birbirine sıkı sıkıya bağlı olmayan, modüler 3 katmanlı yapıda kurgulanmıştır. Pencereler arası iletişim asenkron **PyQt5 Sinyal/Slot (Signal/Slot)** mimarisiyle sağlanır.

## 🚀 Kurulum ve Çalıştırma

### 🔌 Gereksinimler
Sistemi sorunsuz çalıştırabilmek için bilgisayarınızda Python kurulu olması gerekir. Gerekli harici kütüphaneleri terminalinizden tek seferde yükleyebilirsiniz:

```bash
pip install PyQt5 matplotlib numpy
