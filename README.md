# locksmith
This program is a comprehensive tool for analysing your passwords for security and weaknesses. It helps users understand how strong their passwords are, detect common weaknesses and thus better protect their digital identity.

# Şifre Güvenlik Analizi

🔐 **Güvenli şifre oluşturma ve analiz etme aracı** - Modern web teknolojileri ile geliştirilmiş, kullanıcı dostu şifre güvenlik analizi uygulaması.

## 🎯 Özellikler

- ✅ **Gerçek zamanlı şifre analizi** - Yazdığınız şifreyi anında analiz eder
- 📊 **Görsel güç göstergesi** - Progress bar ile şifre gücünü gösterir
- 💬 **Detaylı geri bildirim** - Şifrenizin güçlü ve zayıf yönlerini açıklar
- 💡 **Akıllı öneriler** - Şifrenizi güçlendirmek için öneriler sunar
- 🔍 **Kalıp tespiti** - Güvensiz kalıpları tespit eder
- 🎲 **Güvenli şifre üretici** - Özelleştirilebilir şifre oluşturucu
- 📱 **Responsive tasarım** - Mobil ve desktop uyumlu
- 🌙 **Dark mode desteği** - Karanlık tema desteği
- 🔒 **Gizlilik odaklı** - Şifreleriniz sunucuda saklanmaz

## 🚀 Kurulum

### Gereksinimler
- Python 3.8+
- pip (Python paket yöneticisi)

### Adım 1: Projeyi İndirin
```bash
git clone <repository-url>
cd sifre-analiz
```

### Adım 2: Sanal Ortam Oluşturun (Önerilen)
```bash
python -m venv venv
```

#### Windows:
```bash
venv\Scripts\activate
```

#### macOS/Linux:
```bash
source venv/bin/activate
```

### Adım 3: Bağımlılıkları Yükleyin
```bash
pip install -r requirements.txt
```

### Adım 4: Uygulamayı Çalıştırın
```bash
python app.py
```

Uygulama varsayılan olarak `http://localhost:5000` adresinde çalışacaktır.

## 📱 Kullanım

1. **Şifre Analizi**: Ana sayfada şifrenizi girin ve gerçek zamanlı analiz sonuçlarını görün
2. **Güç Göstergesi**: Şifrenizin güç seviyesini 0-100 arasında görün
3. **Geri Bildirim**: Detaylı geri bildirimleri okuyun
4. **Öneriler**: İyileştirme önerilerini uygulayın
5. **Şifre Oluşturucu**: "Güvenli Şifre Oluştur" butonuna tıklayarak özel şifreler oluşturun

## 🔧 API Endpoints

### Şifre Analizi
```http
POST /api/analyze
Content-Type: application/json

{
  "password": "your_password_here"
}
```

### Şifre Oluşturma
```http
POST /api/generate
Content-Type: application/json

{
  "length": 16,
  "uppercase": true,
  "lowercase": true,
  "digits": true,
  "special": true,
  "exclude_ambiguous": true
}
```

## 🎨 Özelleştirme

### CSS Değişkenleri
`static/css/style.css` dosyasında `:root` bölümündeki CSS değişkenlerini düzenleyerek renkleri ve boyutları özelleştirebilirsiniz.

### Analiz Algoritması
`app.py` dosyasındaki `PasswordAnalyzer` sınıfını düzenleyerek analiz kriterlerini değiştirebilirsiniz.

## 🔒 Güvenlik

- **Client-side odaklı**: Şifreler yalnızca analiz için kullanılır, saklanmaz
- **HTTPS desteği**: Production ortamında HTTPS kullanın
- **CORS koruması**: Cross-origin istekleri kontrol edilir
- **Input validation**: Tüm girişler doğrulanır

## 📊 Analiz Kriterleri

### Şifre Gücü Hesaplama
- **Uzunluk** (0-25 puan): Şifre uzunluğu
- **Karakter Çeşitliliği** (0-30 puan): Farklı karakter türleri
- **Benzersizlik** (0-20 puan): Tekrar eden karakterler
- **Kalıp Kontrolü** (0-25 puan): Güvensiz kalıpların tespiti

### Tespit Edilen Kalıplar
- Ardışık karakterler
- Sayısal diziler
- Alfabetik diziler
- Klavye kalıpları
- Yaygın şifreler
- Tarih formatları

## 🌐 Deployment

### Netlify (Frontend)
1. `static` klasörünü Netlify'a yükleyin
2. API endpoint'lerini güncelleyin

### Heroku (Backend)
1. `Procfile` oluşturun:
```
web: python app.py
```

2. Heroku'ya deploy edin:
```bash
git add .
git commit -m "Deploy to Heroku"
git push heroku main
```

### Docker
```dockerfile
FROM python:3.9-slim

WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

EXPOSE 5000
CMD ["python", "app.py"]
```

## 🤝 Katkıda Bulunma

1. Fork edin
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add amazing feature'`)
4. Branch'i push edin (`git push origin feature/amazing-feature`)
5. Pull Request açın

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.

## 🆘 Destek

Herhangi bir sorunuz veya öneriniz varsa:
- Issue açın
- Email gönderin
- Dokümantasyonu kontrol edin

## 📝 Changelog

### v1.0.0
- ✅ Temel şifre analizi
- ✅ Güvenli şifre oluşturucu
- ✅ Responsive tasarım
- ✅ Dark mode desteği
- ✅ Türkçe dil desteği

## 🙏 Teşekkürler

Bu proje aşağıdaki açık kaynak projeleri kullanmaktadır:
- Flask - Web framework
- Font Awesome - İkonlar
- Google Fonts - Typography

---

Made with ❤️ in Turkey 🇹🇷
