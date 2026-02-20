 Adalı Mahkeme - Beraat Optimizasyon Sistemi

Modern ve interaktif bir web uygulaması ile mahkeme beraat stratejilerini optimize edin!

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML](https://img.shields.io/badge/HTML-5-orange.svg)
![CSS](https://img.shields.io/badge/CSS-3-blue.svg)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow.svg)

Proje Hakkında

Adalı Mahkeme, matematiksel optimizasyon problemini bir senaryo ile birleştiren bir web uygulamasıdır. Kullanıcılar, farklı hâkim ve jüri rüşvet parametreleri girerek en düşük maliyetle beraat etme stratejisini hesaplayabilir.

Senaryo
Bir adada tatildeyken, yerde bıçaklanmış bir adam buluyorsunuz. Yardım etmeye çalışırken ada polisi sizi tutukluyor. Adada farklı işleyen bir adalet sistemi var ve siz en düşük maliyetle beraat etmenin yolunu bulmalısınız.

Mahkeme Kuralları
- **Hâkim "Beraat" verirse** → Direkt serbest kalırsınız
- **Hâkim "Çekimser" kalırsa** → Jürinin %50'sinden fazlası beraat yönünde oy vermeli
- **Hâkim "Suçlu" derse** → Jürinin %100'ü beraat yönünde oy vermeli



Çalıştırma Adımları

Yöntem 1: Doğrudan Tarayıcıda Açma
1. Projeyi bilgisayarınıza indirin veya klonlayın
2. `adali_mahkeme.html` dosyasını bulun
3. Dosyaya çift tıklayın
4. Uygulama varsayılan tarayıcınızda açılacaktır

Terminal/Komut Satırı ile Açma

**Windows:**
```bash
# Proje klasörüne gidin
cd adali-mahkeme

# Dosyayı varsayılan tarayıcıda açın
start adali_mahkeme.html
```

**macOS:**
```bash
# Proje klasörüne gidin
cd adali-mahkeme

# Dosyayı varsayılan tarayıcıda açın
open adali_mahkeme.html
```

**Linux:**
```bash
# Proje klasörüne gidin
cd adali-mahkeme

# Dosyayı varsayılan tarayıcıda açın
xdg-open adali_mahkeme.html
```


## 📁 Proje Yapısı

```
adali-mahkeme/
│
├── adali_mahkeme.html    # Ana uygulama dosyası (tek dosya)
└── README.md             # Proje dokümantasyonu
```

Kullanım Kılavuzu

1. Jüri Bilgilerini Girin
- **Jüri Üye Sayısı:** Mahkemede kaç jüri üyesi olacağını belirleyin
- **Jüri Rüşveti:** Her jüri üyesinin istediği rüşvet miktarını girin

2. Hâkim Rüşvet Tutarlarını Ayarlayın
5 farklı hâkim için:
- **Beraat Rüşveti:** Hâkimin direkt beraat vermesi için gereken tutar
- **Çekimser Rüşveti:** Hâkimin çekimser kalması için gereken tutar

### 3. Optimal Stratejiyi Hesaplayın
"Optimal Stratejiyi Hesapla" butonuna tıklayın.

### 4. Sonuçları İnceleyin
Uygulama size:
- En düşük maliyetli stratejiyi
- Hangi hâkimi seçmeniz gerektiğini
- Hangi senaryoyu uygulamanız gerektiğini
- Tüm hâkimler için karşılaştırmalı analizi gösterecektir

Algoritma Mantığı

Uygulama her hâkim için 3 farklı senaryo hesaplar:

Senaryo 1: Hâkimi Beraat'e İkna Et
```
Maliyet = Hâkim Beraat Rüşveti
Jüri Masrafı = 0
```

Senaryo 2: Hâkimi Çekimser Yap + Jüri Çoğunluğu
```
Jüri Çoğunluk = ⌊Jüri Sayısı / 2⌋ + 1
Maliyet = Hâkim Çekimser Rüşveti + (Jüri Çoğunluk × Jüri Üye Rüşveti)
```

Senaryo 3: Tüm Jüriyi Satın Al
```
Maliyet = Jüri Sayısı × Jüri Üye Rüşveti
Hâkim Masrafı = 0
```

En düşük maliyetli senaryo optimal strateji olarak seçilir.

🙏 Teşekkürler
