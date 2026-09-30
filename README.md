# VelthyraMP

![Version](https://img.shields.io/badge/version-1.0.0-22dd77?style=for-the-badge)
![Distribution](https://img.shields.io/badge/distribution-binary_only-00599C?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white)
![Game](https://img.shields.io/badge/GTA_San_Andreas-US_1.0-4a9eff?style=for-the-badge)
![SA-MP](https://img.shields.io/badge/SA--MP-0.3.DL--R1-f0a83a?style=for-the-badge)
![CEF](https://img.shields.io/badge/CEF-not_required-7b61ff?style=for-the-badge)

VelthyraMP, SA-MP oynarken kullandığım yardımcı sistemleri tek bir ASI dosyasında toplamak için hazırladığım bir moddur. Panel CEF ile açılmıyor; doğrudan oyun ekranının üzerine çiziliyor. Bu yüzden ayrıca tarayıcı, web paneli veya başka bir istemci moduna ihtiyaç duymuyor.

Bu sürüm yalnızca derlenmiş velthyramp.asi dosyasını içerir. Kaynak kodu bu depoda paylaşılmıyor.

> Şu an doğrulanan sürüm: GTA San Andreas US 1.0 ve SA-MP 0.3.DL-R1.

## İçindekiler

- Neler var?
- Kurulum
- Paneli kullanma
- Model ekleme ve önizleme
- Ayar dosyaları
- Antivirüs uyarısı
- Sürüm notları
- Lisans ve destek

## Neler var?

### /vmp paneli

Paneli açmak için sohbetten /vmp yazmanız yeterli. Menü koyu gri/siyah renklere göre tasarlandı; oyun sırasında gözü yormaması ve normal bir SA-MP menüsü gibi durması amaçlandı.

Panelde ENG/TR düğmesi bulunuyor. İlk açılışta ENG geliyor. Dili değiştirdiğinizde seçim data/velthyramp.ini dosyasına yazılıyor; oyunu kapatıp açtığınızda tekrar dil seçmeniz gerekmiyor.

### Yerel modeller

VelthyraModels klasöründeki DFF/TXD dosyaları panelde listelenir. Model adına göre arama yapabilir, dosya durumunu görebilir ve modeli karakterinize uygulamadan önce önizleyebilirsiniz.

Önizleme ekranında modeli SOL ve SAĞ düğmeleriyle döndürebilir, + ile yaklaştırabilir ve − ile uzaklaştırabilirsiniz. Modeli giyme işlemi yalnızca sizin ekranınızda yapılır; sunucudaki gerçek skin ID'si değiştirilmez.

### Oyuncu ve model bilgileri

Oyuncu inceleme bölümünde görünen bir oyuncunun ID'sini girerek skin bilgilerini görebilirsiniz. Model ID'si, temel ID, DFF/TXD adı ve varsa CRC bilgileri panelde gösterilir.

Model sorgulama bölümünde model ID'si, 0x ile başlayan CRC değeri veya DFF/TXD adı kullanılabilir. Standart GTA skinleri için dosyaların orijinal oyun arşivlerinde bulunduğu konum gösterilir.

### Yakındaki modeller

/vmp nearmodels komutu yakındaki oyuncu skinlerini ve SA-MP objelerini listeler. Seçilen öğenin ID'si, türü ve mesafesi gösterilir; desteklenen modeller önizleme alanında görüntülenir.

Yakındaki modeller için skinleri, objeleri, negatif ID'li özel objeleri, pozitif ID'li sunucu objelerini ve GTA standart obje ID'lerini ayrı ayrı filtreleyebilirsiniz.

### Diğer yardımcılar

- F10 ile HUD'u gizleme ve tekrar gösterme
- FPS sınırını kaldırma
- Fare X/Y hassasiyetini eşitleme
- SA-MP diyaloglarında son seçimi hatırlama
- Sohbeti günlük veya oturum dosyası olarak arşivleme
- Sohbet arşivinde kelime arama
- PNG ekran görüntüsünü koruma ve JPG/BMP kopyası oluşturma
- Favori ve son sunucuları kaydetme
- Bağlanmadan önce oyuncu adını yazma
- Çerçevesiz pencere ve monitör seçimi

## Kurulum

1. Releases bölümünden velthyramp.asi dosyasını indirin.
2. Dosyayı gta_sa.exe dosyasının bulunduğu klasöre atın.
3. Oyunda çalışan bir x86 ASI loader bulunduğundan emin olun.
4. GTA ve SA-MP'yi başlatın.
5. Oyuna girdikten sonra /vmp komutunu deneyin.

Güncelleme yaparken oyunu tamamen kapatın. Oyun açıkken Windows ASI dosyasını kullanımda tuttuğu için yeni dosya kopyalanamayabilir.

## Paneli kullanma

| Yapmak istediğiniz | Kullanacağınız yer |
|---|---|
| Paneli açmak | /vmp |
| Yakındaki modelleri açmak | /vmp nearmodels |
| Dili değiştirmek | Sağ üstteki ENG/TR düğmesi |
| Modeli döndürmek | SOL / SAĞ |
| Modeli yaklaştırmak | + |
| Modeli uzaklaştırmak | − |
| HUD'u gizlemek | F10 |
| Paneli kapatmak | Esc veya × |

Yerel model uygulamaları yalnızca oyuncunun kendi ekranında görünür. Sunucunun gerçek skin, obje veya oyuncu verisi değiştirilmez.

## Model ekleme ve önizleme

Model dosyalarının isimleri aynı olmalıdır:

    gta_sa.exe
    ├── velthyramp.asi
    ├── VelthyraModels
    │   ├── mcallen1.dff
    │   └── mcallen1.txd
    └── data
        └── velthyramp.ini

DFF veya TXD dosyasından biri eksikse model eksik görünür ve giyme düğmesi kullanılamaz. Model dosyaları sunucudan indirilmiş değilse panel bunları kendiliğinden oluşturmaz.

Standart 0–300 arası GTA skinleri dışarı çıkarılmaz. Bu kontrol, orijinal oyun dosyalarının gereksiz yere kopyalanmasını önlemek için bulunuyor.

## Ayar dosyaları

Panel ayarları oyun klasöründeki data/velthyramp.ini dosyasına yazılır:

    language=eng
    fps_unlock=0
    mouse_axis=0
    dialog_restore=0
    f10_hide=0

Dosya yoksa ilk çalıştırmada oluşturulur. Bilinmeyen veya bozuk satırlar yok sayılır; diğer ayarlar silinmez.

Favori sunucular data/velthyramp_servers.dat içinde tutulur. Sohbet kayıtları ve dışarı çıkarılan skinler SA-MP kullanıcı belgeleri altına yazılır.

## Antivirüs uyarısı

Bazı antivirüs programları ASI dosyalarını Riskware, HackTool veya Trojan benzeri adlarla işaretleyebilir. Bunun nedeni, ASI'nin GTA işlemine yüklenmesi, oyun belleğine ve oyun dosyalarına erişmesi, Direct3D/SA-MP işlevleriyle birlikte çalışması ve ayar dosyaları oluşturmasıdır. Bu davranışlar kötü amaçlı yazılımlarda da görülebildiği için davranışsal taramalar yanlış pozitif üretebilir.

Bu uyarı dosyanın kesin olarak virüs olduğu anlamına gelmez.
ChatGPT, Claude veya Gemini gibi araçlar ile dosya hakkında detaylı açıklama ve bilgi alabilirsiniz.

## Dağıtım içeriği

Bu depoda yalnızca aşağıdaki binary bulunur:

    velthyramp.asi

Kaynak kodu, derleme betikleri, test dosyaları, debug sembolleri ve geliştirici bilgisayarına ait yollar dağıtıma dahil değildir.

## Sürüm notları

### 1.0.0

- ENG/TR dil seçimi kalıcı hale getirildi.
- Dil seçimi data/velthyramp.ini dosyasına yazılmaya başlandı.
- Panel yeniden açıldığında son kullanılan dil yükleniyor.
- Koyu temalı /vmp paneli düzenlendi.
- Yerel model arama ve 3B önizleme eklendi.
- Yakındaki skin ve obje listesi geliştirildi.
- Model döndürme ve yakınlaştırma düğmeleri eklendi.
- F10 HUD kontrolü, sohbet arşivi ve sunucu merkezi tamamlandı.

### 0.9.x

- İlk kapsamlı CEF'siz panel altyapısı.
- Yerel model kataloğu ve DFF/TXD kontrolleri.
- Oyuncu/model inceleme ekranları.
- Yakındaki model filtreleri.
- Çerçevesiz pencere yöneticisi.

## Lisans ve destek

VelthyraMP kapalı kaynak binary dağıtımıdır. Dosyanın değiştirilmiş veya yeniden paketlenmiş sürümlerini resmi sürüm olarak paylaşmayın.

Hata bildirirken GTA ve SA-MP sürümünü, kullandığınız ASI/CLEO modlarını ve hatanın ne zaman oluştuğunu yazın. Kullanıcı adınızı, IP adresinizi ve bilgisayarınızdaki özel klasör yollarını paylaşmadan önce mutlaka silin.

---

VelthyraMP Development Team — 2026
