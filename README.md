# GraduationProject-Backend

<p align="center">
  <img src="https://img.shields.io/badge/Java-17-orange?logo=java&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/SpringBoot-3.1-green?logo=spring&logoColor=white" alt="Spring Boot">
</p>

Documentation version of our graduation project: Digital-Based Complaint and Tracking System for Municipalities.

This project is a Spring Boot microservice backend application designed as a Digital Based Complaint and Tracking System for Municipalities. The system ensures that complaints and requests submitted by citizens to the municipality are recorded, tracked and shared with relevant units. The backend side is structured with a microservice architecture, and each module has its own area of ​​responsibility.

Communication for the project and code --> ensekr78@gmail.com

Bu proje, Belediyeler İçin Dijital Tabanlı Şikayet ve Takip Sistemi olarak tasarlanmış bir Spring Boot mikroservis backend uygulamasıdır. Sistem, vatandaşların belediyeye ilettikleri şikayet ve taleplerin kaydedilmesini, takibini ve ilgili birimlerle paylaşılmasını sağlar. Backend tarafı mikroservis mimarisi ile yapılandırılmış olup, her modül kendi sorumluluk alanına sahiptir.

Repo, Spring Boot kullanılarak geliştirilmiş mikroservis tabanlı bir backend uygulamasının dökümantasyon sürümüdür.
Güvenlik ve gizlilik nedenleriyle gerçek kodlar eklenmemiştir, yalnızca mimari yapılar, tablolar ve API taslakları belgelenmiştir.

Projenin ve kodun tamamı için iletişim --> ensekr78@gmail.com

## 🚀 Mimari

Uygulama, katmanlı ve mikroservis mimarisi prensipleriyle geliştirilmiştir:

Controller → Service → Repository → Database

DTO ve Response objeleri ile veri taşınımı

İş kuralları ve veri yönetimi Service katmanında

Repository katmanı Spring Data JPA kullanılarak veritabanı işlemlerini yönetir


## 🛠 Temel Modüller ve Özellikler

### Şikayet ve Talep Yönetimi
• Vatandaşlar uygulama üzerinden şikayet veya talep oluşturabilir.  
• Her şikayet, başlık, açıklama, fotoğraf ve konum bilgisi ile kaydedilir.  
• Yetkili birimler, şikayetleri inceleyip durum güncellemelerini yapabilir.  
• Her şikayetin durumu **Yeni, İnceleniyor, Çözüldü** olarak takip edilir.  

### Kullanıcı Yönetimi
• Kullanıcı kayıt ve giriş işlemleri **JWT tabanlı oturum yönetimi** ile güvence altına alınmıştır.  
• Kullanıcı rolleri: **Vatandaş, Belediye Personeli, Yönetici**  
• Yetkilendirme, roller ve izinlere dayalıdır.  

### Bildirim ve Takip Modülü
• Şikayet sahipleri, durum değişikliklerinden bildirim alır.  
• Belediye personeli, atanmış şikayetlerin takibini sistem üzerinden yapabilir.  
• Günlük veya haftalık raporlar üretilebilir.  

### Teknik Altyapı ve Entegrasyon
• **Backend:** Java 17 + Spring Boot + Spring Data JPA  
• **Veritabanı:** MySQL (demo ve canlı kullanım için)  
• **API Katmanı:** RESTful, JSON tabanlı  
• **Mikroservisler:** Kullanıcı yönetimi, şikayet yönetimi, bildirim servisi  
• **Güvenlik:** JWT, HTTPS, veri doğrulama ve şifreleme  
