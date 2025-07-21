Roltek Stajyer Teknik Case: Device Management API (Fullstack)

Bu proje, Roltek Teknoloji'nin IoT tabanlı ürün ve servis ortamına yönelik olarak hazırlanmıştır. Adayın, Spring Boot ve React (Next.js + TypeScript) kullanarak fullstack geliştirme becerilerini değerlendirmek amacıyla oluşturulmuştur.

🔧 Proje Hakkında

Kullanıcıların sisteme giriş yaparak kendi cihazlarını yönetebildiği (CRUD işlemleri) bir cihaz yönetim sistemidir.

🧠 Değerlendirme Kriteri

Eğer aday daha önce Spring Boot ve React kullanarak geliştirdiği ve:

Yayına alınmış bir proje sunabiliyorsa,

Veya Docker ile çalıştırılabilir şekilde bir proje hazırladıysa,

Bu case yerine o projenin detaylı bir README.md dosyası ile birlikte paylaşılması daha değerli kabul edilir.

📁 Proje Yapısı

.
├── backend/    # Spring Boot (Java)
└── frontend/   # Next.js (React + TypeScript)

🚀 Başlangıç Adımları

1. Backend (Spring Boot)

Gereksinimler

Java 17+

Maven

H2 veya PostgreSQL

Kurulum

cd backend
./mvnw spring-boot:run

Özellikler

JWT tabanlı kimlik doğrulama

BCrypt ile şifreleme

CRUD API:

POST /auth/login

GET /devices

GET /devices/{id}

POST /devices

PUT /devices/{id}

DELETE /devices/{id}

Veri Modeli

Device {
  UUID id;
  String name;
  String type;          // SENSOR, CAMERA, LIGHT, etc.
  String serialNumber;  // unique
  LocalDateTime createdAt;
  UUID userId;          // owner reference
}

2. Frontend (Next.js + React + TypeScript)

Gereksinimler

Node.js 18+

pnpm / yarn / npm

Kurulum

cd frontend
pnpm install
pnpm dev

Sayfalar

/login: E-posta ve şifre ile giriş

/devices: Cihaz listeleme, ekleme, düzenleme ve silme işlemleri

Teknik Özellikler

JWT token (localStorage veya HTTP-only cookie ile)

Giriş yapılmadan /devices sayfasına erişim engeli

Form validasyonu ve hata mesajları

Responsive, sade ve anlaşılır kullanıcı arayüzü

🧪 Bonus Özellikler (Opsiyonel)

📝 Teslimat

GitHub repository linki

Bu README.md dosyasının eksiksiz hali

Backend ve frontend dizinleri çalıştırılabilir şekilde yapılandırılmış olmalıdır

👋 İletişim

Her türlü soru ve teknik destek için: info@roltek.com.tr

