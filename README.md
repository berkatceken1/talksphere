# TalkSphere - Real-Time Chat Application

TalkSphere, modern web teknolojileri kullanılarak geliştirilmiş bir real-time chat uygulamasıdır.

## 🚀 Başlangıç

Bu talimatlar, projeyi local geliştirme ortamınızda çalıştırmanız için size yol gösterecektir.

### Ön Gereksinimler

- Node.js (v14 veya üzeri)
- MongoDB hesabı
- Git

### ⚙️ Kurulum

1. Projeyi klonlayın

```bash
git clone https://github.com/berkatceken1/talksphere.git
cd talksphere
```

2. Bağımlılıkları yükleyin

```bash
npm install
```

3. Environment Variables Ayarları
   - `.env.example` dosyasını `.env` olarak kopyalayın
   - `.env` dosyasını aşağıdaki değişkenlerle güncelleyin:

```bash
MONGO_URI=your_mongodb_connection_string
PORT=3000
JWT_SECRET=your_jwt_secret
NODE_ENV=development
```

**🔐 Önemli Notlar:**

- `MONGO_URI`: MongoDB Atlas'tan alınacak bağlantı string'i
  - MongoDB Atlas'ta yeni bir proje oluşturun
  - Database Access'ten yeni bir kullanıcı oluşturun
  - Network Access'ten IP adresinizi ekleyin (veya 0.0.0.0/0 ile tüm IP'lere izin verin)
  - Clusters'tan "Connect" butonuna tıklayıp connection string'i alın
- `JWT_SECRET`: Güvenli bir string belirleyin (örn: uzun ve karmaşık bir parola)

4. Uygulamayı çalıştırın

```bash
npm run dev
```

Uygulama varsayılan olarak `http://localhost:3000` adresinde çalışacaktır.

## 🛠️ API Endpoints

### Auth Routes

- `POST /api/v1/auth/signup` - Yeni kullanıcı kaydı
- `POST /api/v1/auth/login` - Kullanıcı girişi
- `POST /api/v1/auth/logout` - Kullanıcı çıkışı

## 🔧 Teknolojiler

- Express.js - Backend framework
- MongoDB - Veritabanı
- JWT - Authentication
- bcrypt - Şifreleme
- Cookie-parser - Cookie yönetimi
