# Proje Ödevi 2. Adım: Bilgi Mimarisi ve Arayüz Tasarımı

## Proje Adı: "Risona"

### 1. Site Haritası / Ekran Akış Diyagramı

Platformun temel navigasyon yapısı ve ekranlar arası geçişler aşağıda listelenmiştir.

* **Herkese Açık Sayfalar (Giriş Yapılmamış):**
    * **/ (Ana Sayfa):**
        * Öne çıkan müzisyenler.
        * Yaklaşan etkinlikler.
        * Keşfetmeye yönelik arama çubuğu.
        * Giriş Yap / Kayıt Ol butonları.
    * **/kesfet (Keşfet Sayfası):**
        * Tüm müzisyenlerin listelendiği sayfa.
        * Filtreleme seçenekleri (Şehir, Müzik Türü).
        * Sıralama seçenekleri (Popüler, Yeni).
    * **/etkinlikler (Etkinlikler Sayfası):**
        * Tüm etkinliklerin takvim veya liste görünümü.
    * **/muzisyen/[profil-adi] (Müzisyen Detay Sayfası):**
        * Müzisyenin herkese açık profil sayfası.
    * **/giris (Giriş Yap Sayfası)**
    * **/kayit-ol (Kayıt Ol Sayfası):**
        * Kullanıcıya "Müzisyen" veya "Dinleyici" olarak kayıt olma seçeneği sunar.

* **Giriş Yapmış Kullanıcı (Dinleyici) Sayfaları:**
    * **/panel/takiplerim (Takip Ettiklerim):**
        * Takip ettiği müzisyenlerin son aktiviteleri.
    * **/panel/hesabim (Hesap Ayarları):**
        * Profil bilgileri ve şifre değiştirme.

* **Giriş Yapmış Kullanıcı (Müzisyen) Sayfaları:**
    * **/panel/profilimi-duzenle (Profilimi Düzenle):**
        * Biyografi, resim, sosyal medya linklerini düzenleme.
        * Müzik linklerini (YouTube, SoundCloud) ekleme/çıkarma.
    * **/panel/etkinliklerim (Etkinliklerim):**
        * Yeni etkinlik ekleme, mevcutları düzenleme/silme.

### 2. Kullanıcı Rolleri ve Yetkiler

| Eylem / Sayfa Erişimi          | Ziyaretçi (Giriş Yapmamış) | Dinleyici (Giriş Yapmış) | Müzisyen (Giriş Yapmış)  |
| ------------------------------ | -------------------------- | ------------------------ | ------------------------ |
| Müzisyenleri Görüntüleme       | ✅ Evet                    | ✅ Evet                  | ✅ Evet                  |
| Etkinlikleri Görüntüleme       | ✅ Evet                    | ✅ Evet                  | ✅ Evet                  |
| Müzisyen Profillerine Bakma    | ✅ Evet                    | ✅ Evet                  | ✅ Evet                  |
| Müzisyen Takip Etme            | ❌ Hayır                   | ✅ Evet                  | ✅ Evet                  |
| Kendi Profilini Düzenleme      | ❌ Hayır                   | ✅ Evet (Dinleyici profili) | ✅ Evet (Müzisyen profili)|
| Yeni Etkinlik Oluşturma        | ❌ Hayır                   | ❌ Hayır                 | ✅ Evet                  |

### 3. Wireframe (Taslak Çizim) Açıklamaları

Aşağıda, uygulamanın üç temel ekranı için basit metin tabanlı wireframe açıklamaları bulunmaktadır.

---

**Wireframe 1: Ana Sayfa**
+----------------------------------------------------------------------+
| [Risona LOGO]   [Keşfet]   [Etkinlikler]     [Giriş Yap] [Kayıt Ol]   |
+----------------------------------------------------------------------+
|                                                                      |
|                  YENİ SESLER KEŞFET                                  |
|                  [ Şehir veya Müzik Türü Ara...  ] [ARA]             |
|                                                                      |
+----------------------------------------------------------------------+
|                                                                      |
|   Öne Çıkan Sanatçılar |
|   +----------+   +----------+   +----------+   +----------+          |
|   | [Resim]  |   | [Resim]  |   | [Resim]  |   | [Resim]  |          |
|   | Sanatçı A|   | Sanatçı B|   | Sanatçı C|   | Sanatçı D|          |
|   | Pop/Rock |   |   Indie  |   |  Elekro  |   |   Jazz   |          |
|   +----------+   +----------+   +----------+   +----------+          |
|                                                                      |
+----------------------------------------------------------------------+
|                                                                      |
|   Yaklaşan Etkinlikler |
|   - [Tarih] Konser Adı - Sanatçı A @ Mekan X                         |
|   - [Tarih] Akustik Gece - Sanatçı C @ Mekan Y                       |
|   - [Tarih] Festival - Çeşitli Sanatçılar @ Mekan Z                  |
|                                                                      |
+----------------------------------------------------------------------+
| [Hakkında] [İletişim] [Sosyal Medya Linkleri]                        |
+----------------------------------------------------------------------+


---

**Wireframe 2: Keşfet Sayfası**

+----------------------------------------------------------------------+
| [Risona LOGO]   [Keşfet]   [Etkinlikler]         [Hesabım] [Çıkış]    |
+----------------------------------------------------------------------+
|                                                                      |
|   Filtrele: [Tüm Şehirler v]  [Tüm Türler v]   Sırala: [Popüler v]    |
|                                                                      |
+----------------------------------------------------------------------+
|                                                                      |
| +------------------+  +------------------+  +------------------+     |
| | [Resim]          |  | [Resim]          |  | [Resim]          |     |
| | Sanatçı Adı 1|  | Sanatçı Adı 2|  | Sanatçı Adı 3|     |
| | Pop/Rock - Şehir |  | Indie - Şehir    |  | Jazz - Şehir     |     |
| | [Profili Gör ->] |  | [Profili Gör ->] |  | [Profili Gör ->] |     |
| +------------------+  +------------------+  +------------------+     |
|                                                                      |
| +------------------+  +------------------+  +------------------+     |
| | [Resim]          |  | [Resim]          |  | [Resim]          |     |
| | Sanatçı Adı 4|  | Sanatçı Adı 5|  | Sanatçı Adı 6|     |
| | ...              |  | ...              |  | ...              |     |
| +------------------+  +------------------+  +------------------+     |
|                                                                      |
+----------------------------------------------------------------------+


---

**Wireframe 3: Müzisyen Detay Sayfası**

+----------------------------------------------------------------------+
| [Risona LOGO]   [Keşfet]   [Etkinlikler]         [Hesabım] [Çıkış]    |
+----------------------------------------------------------------------+
|                                                                      |
|  [Büyük Profil Resmi]  SANATÇI ADI [TAKİP ET +]                  |
|                        Indie/Rock - Şehir |
|                        [YT] [IG] [SP] (Sosyal Medya İkonları)        |
|                                                                      |
|  "Sanatçının kısa biyografisi burada yer alacak. Müzik yolculuğu,   |
|  ilham kaynakları ve tarzı hakkında bilgiler..."                     |
|                                                                      |
+----------------------------------------------------------------------+
|                                                                      |
|   Müzikleri |
|   > [Oynat] Şarkı Adı 1 (SoundCloud Gömülü Player)                   |
|   > [Oynat] Şarkı Adı 2 (YouTube Gömülü Player)                      |
|                                                                      |
+----------------------------------------------------------------------+
|                                                                      |
|   Yaklaşan Etkinlikleri |
|   - [Tarih] Konser Adı @ Mekan X                                     |
|                                                                      |
+----------------------------------------------------------------------+
