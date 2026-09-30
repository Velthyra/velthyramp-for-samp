# VelthyraMP

![Version](https://img.shields.io/badge/version-1.0.0-22dd77?style=for-the-badge)
![Distribution](https://img.shields.io/badge/distribution-binary_only-00599C?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white)
![Game](https://img.shields.io/badge/GTA_San_Andreas-US_1.0-4a9eff?style=for-the-badge)
![SA-MP](https://img.shields.io/badge/SA--MP-0.3.DL--R1-f0a83a?style=for-the-badge)
![CEF](https://img.shields.io/badge/CEF-not_required-7b61ff?style=for-the-badge)

VelthyraMP, GTA San Andreas 1.0 US ve SA-MP 0.3.DL-R1 için dağıtılan bağımsız bir x86 ASI eklentisidir. CEF kullanmadan çalışan koyu temalı oyun içi panel; model önizleme, yakındaki model taraması, sohbet arşivi, ekran görüntüsü, HUD yardımcıları ve sunucu merkezi özelliklerini tek bir ASI dosyasında toplar.

VelthyraMP bağımsız çalışır. Kaynak kodu bu dağıtımda paylaşılmaz; kullanıcıya yalnızca derlenmiş velthyramp.asi dosyası sunulur.

> Geliştirme durumu: Aktif geliştirme aşamasındadır. GTA belleğine ve SA-MP sürümüne bağlı özellikler, farklı ASI, CLEO ve grafik modlarıyla birlikte ayrıca test edilmelidir.

---

## İçindekiler

- [Özellikler](#özellikler)
- [Gereksinimler](#gereksinimler)
- [Kurulum](#kurulum)
- [Panel kullanımı](#panel-kullanımı)
- [Model sistemi](#model-sistemi)
- [Ayarlar ve veri dosyaları](#ayarlar-ve-veri-dosyaları)
- [Dağıtım içeriği](#dağıtım-içeriği)
- [Güvenlik ve gizlilik](#güvenlik-ve-gizlilik)
- [Changelog](#changelog)
- [Lisans ve destek](#lisans-ve-destek)

---

## Özellikler

### Panel ve yerelleştirme

- CEF gerektirmeyen Direct3D 9 tabanlı koyu tema.
- ENG/TR dil seçimi ve kalıcı dil tercihi.
- Fare, Tab, Enter ve Esc ile gezinme.
- Türkçe klavye düzeni, Ctrl+A, Ctrl+V, Home/End ve ok tuşu desteği.
- Panel durum mesajlarının seçilen dile göre gösterilmesi.

### Model ve skin araçları

- VelthyraModels klasöründeki DFF/TXD çiftlerini otomatik kataloglama.
- Model adına göre arama ve liste filtreleme.
- Dosya boyutu, dosya durumu ve DFF/TXD CRC bilgileri.
- Modeli karaktere uygulamadan 3B önizleme.
- Sol/sağ döndürme ve +/− yakınlaştırma kontrolleri.
- Oyuncu ID'siyle görünür oyuncu skin bilgisi inceleme.
- Model ID, CRC, DFF veya TXD adıyla sorgulama.
- Seçilen modeli yalnızca kendi ekranında başka oyuncuya uygulama.
- Orijinal yerel görünümü geri yükleme.
- Standart 0–300 skinlerinin yanlışlıkla çıkarılmasını önleme.

### Yakındaki modeller

- Yakındaki yüklenmiş oyuncu skinlerini ve SA-MP objelerini listeleme.
- Mesafe, model ID'si, tür ve kaynak bilgisi.
- Skin/obje görünürlüğü için bağımsız filtreler.
- Negatif özel obje ID'lerini açma/kapatma.
- Pozitif sunucu objelerini açma/kapatma.
- GTA standart obje ID'lerini ayrı filtreleme.
- Seçilen öğeyi önizleme ve ayrıntılarını görüntüleme.

### Oyun yardımcıları

- F10 ile HUD gizleme ve tekrar gösterme.
- FPS sınırı ve fare X/Y dengesi.
- SA-MP diyalog seçimlerini hatırlama.
- PNG ekran görüntüsünü koruma ve isteğe bağlı JPG/BMP kopyası.
- Sohbet arşivi, günlük/oturum dosyası ve sohbet içinde arama.
- Favori ve son sunucular için sunucu merkezi.
- Bağlantı öncesi oyuncu adı girişi.
- Çerçevesiz pencere ve hedef monitör seçimi.

---

## Gereksinimler

- Windows 10 veya üzeri
- GTA San Andreas US 1.0, 32 bit
- SA-MP 0.3.DL-R1
- Çalışan bir ASI loader
- x86 ASI loader

Eklenti yalnızca GTA San Andreas US 1.0 ve SA-MP 0.3.DL-R1 üzerinde doğrulanmıştır. x64 istemciler desteklenmez.

---

## Kurulum

1. Release bölümünden yalnızca velthyramp.asi dosyasını indirin.
2. Dosyayı gta_sa.exe dosyasının bulunduğu klasöre kopyalayın.
3. Oyunu ve SA-MP'yi başlatın.
4. Sohbette /vmp yazarak paneli açın.
5. /vmp nearmodels ile Yakındaki modeller sayfasına geçin.

İlk çalıştırmada dil ENG olarak başlar. Sağ üstteki ENG düğmesine basıldığında TR seçimi data/velthyramp.ini dosyasına kaydedilir ve sonraki açılışlarda korunur.

Oyun çalışırken ASI değiştirmeyin. Windows dosyayı kullanımda tuttuğu için güncellemeden önce GTA'yı kapatın.

---

## Panel kullanımı

| İşlem | Kullanım |
|---|---|
| Paneli aç | /vmp |
| Yakındaki modeller | /vmp nearmodels |
| Dil değiştir | Sağ üstteki ENG/TR düğmesi |
| Modeli döndür | Sol / Sağ |
| Modeli yakınlaştır | + |
| Modeli uzaklaştır | − |
| Paneli kapat | Esc veya × |
| HUD gizle/göster | F10 |

Yerel model uygulamaları yalnızca oyuncunun kendi ekranında görünür. Sunucunun gerçek skin, obje veya oyuncu verisi değiştirilmez.

---

## Model sistemi

Yerel model klasöründe DFF ve TXD dosyalarının aynı ada sahip olması gerekir:

    gta_sa.exe
    ├── velthyramp.asi
    ├── VelthyraModels
    │   ├── model_adi.dff
    │   └── model_adi.txd
    └── data
        └── velthyramp.ini

Bir dosya çifti eksikse model hatalı görünür ve Giy işlemi devre dışı bırakılır. Önizleme, sunucunun gerçek skin ID'sini değiştirmeden yerel görüntü oluşturur.

---

## Ayarlar ve veri dosyaları

VelthyraMP ayarları oyun klasöründeki data/velthyramp.ini içinde tutulur:

    language=eng
    fps_unlock=0
    mouse_axis=0
    dialog_restore=0
    f10_hide=0

Eksik veya bilinmeyen satırlar yok sayılır. Favori ve son sunucu kayıtları data/velthyramp_servers.dat dosyasındadır. Sohbet arşivi ve çıkarılan skinler SA-MP kullanıcı belgeleri altında tutulur.

---

## Dağıtım içeriği

Bu GitHub dağıtımında yalnızca aşağıdaki dosya bulunur:

    velthyramp.asi

Kaynak kodu, derleme betikleri, test dosyaları, debug sembolleri ve geliştiriciye özel yapılandırmalar dağıtıma dahil değildir.

---

## Güvenlik ve gizlilik

- Bu depoda kaynak kodu veya geliştirici bilgisayarı bulunmaz.
- Kullanıcı ayarları yalnızca kendi oyun klasöründeki data/velthyramp.ini dosyasına yazılır.
- Sohbet arşivi ve model dosyaları kullanıcı bilgisayarında tutulur; bu ASI tarafından GitHub'a yüklenmez.
- Eklentinin içine parola, token veya private key gömülmemelidir.
- ASI dosyası binary olduğu için tersine mühendislik tamamen engellenemez; istemci içine gizli bilgi koymayın.

---

## Changelog

### 1.0.0

- ENG/TR dil seçimi kalıcı ayarlara bağlandı.
- Dil seçimi data/velthyramp.ini içine yazılır.
- Panel yeniden açıldığında son seçilen dil yüklenir.
- Dil kayıt mesajları yerelleştirildi.

### 0.9.0

- CEF'siz kapsamlı /vmp paneli.
- Yerel ve yakındaki model önizlemesi.
- Oyuncu/model inceleme ekranları.
- Sunucu merkezi ve çerçevesiz pencere yöneticisi.
- Yakındaki model filtreleri.

### 0.7.x

- Model kataloglama ve DFF/TXD dışarı çıkarma.
- Sohbet arşivi ve arama.
- Ekran görüntüsü seçenekleri.
- F10 HUD gizleme.
- Ayarların kalıcı dosyaya taşınması.

---

## Lisans ve destek

VelthyraMP kapalı kaynak binary dağıtımıdır. Yeniden paketleme, dosyanın değiştirilmesi veya başka bir ürünün parçası olarak dağıtılması için proje sahibinin izni gerekir.

Hata bildirimlerinde GTA/SA-MP sürümünü, yüklü ASI/CLEO listesini ve çökme zamanını paylaşın. Kullanıcı adı, IP adresi ve özel dosya yollarını maskeleyin.

---

*VelthyraMP Development Team — 2026*
