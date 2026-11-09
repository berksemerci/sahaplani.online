# Saha Planı

**Saha Planı**, halı saha ve amatör futbol takımlarının maç öncesi yerleşimlerini, savunma eşleşmelerini ve hücum koşularını görsel olarak planlamasını sağlayan mobil uyumlu bir taktik tahtasıdır.

7v7, 8v8, 9v9, 10v10 ve 11v11 kadrolar desteklenir. Uygulama kurulum veya üyelik gerektirmeden doğrudan tarayıcıda çalışır.

## Neler yapılabilir?

- Oyuncu adı, forma numarası ve mevki bilgilerini düzenleme
- Kaleci, Defans, Ortasaha ve Forvet mevkileri
- Sınırsız yedek oyuncu ekleme
- Oyuncuları sahada sürükleyip bırakarak serbestçe konumlandırma
- Sahadaki oyuncuya dokunarak yedekle hızlı değişiklik yapma
- Oyuncu değişikliğinde saha konumunu ve savunma eşleşmesini koruma
- Kadro büyüklüğüne uygun hazır dizilişler kullanma
- Adam adama savunma eşleşmeleri oluşturma
- Alan savunması bölgeleri çizme
- Koşu ve pas yönlerini oklarla gösterme
- Kendi takımının forma rengini seçme
- Rakip forma rengini otomatik olarak karşıt renkte belirleme
- Rakip oyuncuların görünürlüğünü ayarlama
- Rakip oyuncuları ve eşleştirme araçlarını tamamen açıp kapatma
- Birbiriyle kesişmeyen alan savunması bölgeleri oluşturma
- Serbest çizim aracıyla özel hareket ve taktik işaretleri ekleme
- Araç çubuğu veya `Ctrl+Z` / `Ctrl+Y` ile geri alma ve yineleme
- Aynı takımda tekrarlanan forma numaralarını engelleme
- Maç planına taktik notları ekleme
- Tüm tahtayı ve notları PNG görseli olarak paylaşma
- Taktiği JSON dosyası olarak yedekleme ve geri yükleme
- Değişiklikleri tarayıcıda otomatik saklama

## Kullanım

1. Sol üstteki kadro seçicisinden maç formatını belirleyin.
2. **Bizim takım** ve **Rakip** sekmelerinden oyuncuları düzenleyin.
3. Oyuncuları saha üzerinde sürükleyerek istediğiniz yerleşimi oluşturun.
4. Hızlı oyuncu değişikliği için sahadaki oyuncuya kısa dokunup yerine girecek yedeği seçin.
5. **Ok**, **Alan** ve **Eşleştir** araçlarıyla taktik detaylarını ekleyin.
6. Taktik notlarını sağ paneldeki alana yazın.
7. **Görseli paylaş** ile bütün planı tek PNG dosyası hâline getirin.

İlk ziyarette açılan kısa kullanım rehberi, **Yardım** düğmesiyle tekrar görüntülenebilir.

## Ayarlar ve yedekleme

**Ayarlar** bölümünden:

- Rakip oyuncuların saydamlığı değiştirilebilir.
- Mevcut taktik `.json` dosyası olarak yedeklenebilir.
- Daha önce alınan bir taktik yedeği geri yüklenebilir.
- Tahta tamamen sıfırlanabilir.

Yedek dosyası; oyuncuları, forma renklerini, saha yerleşimini, çizimleri, eşleşmeleri ve taktik notlarını birlikte içerir.

## Teknik yapı

Proje bağımlılık veya derleme süreci gerektirmeyen statik bir web uygulamasıdır.

```text
index.html       Uygulama arayüzü
app.js           Taktik tahtası ve veri yönetimi
styles.css       Ana görünüm ve saha tasarımı
kits.css         Forma renk seçimi
settings.css     Ayarlar penceresi
tour.css         İlk kullanım rehberi
assets/          Logo ve görsel varlıklar
vercel.json      Vercel yayın ayarları
```

Oyuncu ve taktik verileri varsayılan olarak tarayıcının `localStorage` alanında tutulur. Harici bir veritabanına gönderilmez.

## Yerel çalıştırma

Projeyi klonladıktan sonra kök dizini herhangi bir statik dosya sunucusuyla açabilirsiniz:

```bash
npx serve .
```

Ardından terminalde gösterilen yerel adresi tarayıcıda açın.

## Vercel ile yayınlama

1. GitHub deposunu Vercel projesine bağlayın.
2. Framework Preset değerini **Other** olarak bırakın.
3. Build Command alanını boş bırakın.
4. Output Directory alanını `.` olarak ayarlayın veya boş bırakın.
5. Production Branch olarak `main` dalını kullanın.
6. Vercel projesinin Domains bölümünden `sahaplani.online` alan adını ekleyin.

`main` dalına gönderilen her güncelleme Vercel tarafından otomatik olarak yeniden yayımlanır.

## Alan adı

**Planlanan canlı adres:** [sahaplani.online](https://sahaplani.online)

Alan adının DNS kayıtları, Vercel projesinin **Domains** ekranında gösterilen güncel değerlere göre yapılandırılmalıdır.

## Lisans

Bu proje özel kullanım için geliştirilmiştir. İzinsiz kopyalama, yeniden dağıtma veya ticari kullanım hakkı vermez.
