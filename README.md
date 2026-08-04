# UDF# (UDF Sharp) Kullanım Kılavuzu

Bu kılavuz, UDF# (UDF Sharp) uygulamasının amacı, sunduğu işlevler ve kullanım şekli hakkında bilgi vermek amacıyla hazırlanmıştır.

## 1. Giriş

UDF#, yapay zekâ destekli geliştirme araçlarından yararlanılarak geliştirilmiş bir masaüstü uygulamasıdır. Uygulamanın ortaya çıkış noktası, mesleki faaliyetler sırasında kullanılan mobil UYAP Editör uygulamasında karşılaşılan bazı eksiklikler ve bu eksikliklere yönelik çözüm arayışıdır.

Bu süreçte geliştirilen UDF+ mobil uygulaması zamanla masaüstü ortamına taşınmış ve UDF# projesinin temelini oluşturmuştur. Windows platformunda sınırlı düzeyde geliştirme deneyimine sahip olmama rağmen, geliştirme sürecini daha iyi anlayabildiğim ve yönetebildiğim için doğrudan Windows uygulaması geliştirmeyi tercih ettim. Yapay zekâ araçları geliştirme sürecini önemli ölçüde hızlandırsa da, ortaya çıkan ürünün sağlıklı biçimde geliştirilebilmesi için yazılım geliştirme mantığının anlaşılmasının gerekli olduğu kanaatindeyim.

## 2. Uygulamanın Amacı ve İşlevleri

### 2.1 Amaç

UDF#, temel olarak UDF dosyaları üzerinde dönüştürme işlemleri gerçekleştirmek amacıyla geliştirilmiştir. Bunun yanında, deneysel nitelikte bazı düzenleme işlevleri de sunmaktadır. Ancak uygulama bir belge editörü değildir. Metin düzenleme işlemleri, UDF dosyası içerisindeki belirli metinlerin bulunup yeni değerlerle değiştirilmesi mantığıyla çalışmaktadır.

### 2.2 İşlevler

UDF# aşağıdaki temel işlevleri sunmaktadır:

#### Word Belgelerini UDF'ye Dönüştürme

Uygulama; DOCX, DOC ve RTF uzantılı belgelerin UDF formatına dönüştürülmesini destekler.

Dönüştürme işlemi;

* Uygulama arayüzü üzerinden,
* Dosyaların sağ tık menüsüne eklenen bağlam menüsü seçenekleri üzerinden

gerçekleştirilebilir.

Arayüz üzerinden yapılan dönüştürmelerde çıktı klasörü seçilebilir. Bağlam menüsü kullanıldığında ise çıktı dosyaları doğrudan kaynak dosyanın bulunduğu klasöre oluşturulur. Her iki yöntem de toplu dosya dönüştürmeyi desteklemektedir.

Dönüştürme işlemi sırasında belgenin biçimsel yapısının mümkün olduğunca korunması hedeflenmektedir. Metin biçimlendirmeleri (kalın, italik, altı çizili vb.), paragraf özellikleri, tablolar ve resimler dönüştürme sırasında korunarak UDF belgesine aktarılmaktadır. Amaç, oluşturulan UDF dosyasının kaynak Word belgesiyle görsel ve yapısal açıdan mümkün olduğunca uyumlu olmasını sağlamaktır. Ancak UDF formatının teknik sınırlamaları nedeniyle bazı özel biçimlendirmeler veya Word'e özgü özellikler birebir aktarılamayabilir.

#### UDF Dosyalarını PDF'ye Dönüştürme

UDF dosyaları uygulama arayüzünden veya bağlam menüsü üzerinden PDF formatına dönüştürülebilir. İşlem tek dosya veya çoklu dosya üzerinde gerçekleştirilebilir.

Benzer bir işlem UYAP Doküman Editörü ile de yapılabilmektedir. Ancak oluşturulan PDF dosyalarında görsel içerik doğru şekilde korunmasına rağmen, eklenen metin katmanında Türkçe karakter desteği bulunmamaktadır. Bu nedenle UDF# içerisinde alternatif bir PDF dönüştürme özelliği geliştirilmiştir.

Bu özellik hâlen beta aşamasındadır ve geliştirme çalışmaları devam etmektedir.

#### UDF Dosyalarında Metin Değiştirme

Bu özellik uygulamada iki ayrı sekme altında sunulmaktadır:

* Tek Belge
* Çoklu Belge

**Tek Belge** sekmesinde seçilen bir UDF dosyası içerisinde belirli bir metin aranabilir ve bulunan metin birden fazla farklı değerle değiştirilebilir. Girilen her yeni değer için ayrı bir UDF dosyası oluşturulur.

**Çoklu Belge** sekmesinde ise birden fazla UDF dosyası içerisinde arama yapılabilir ve bulunan metin tek bir yeni değer ile değiştirilebilir. Her kaynak belge için ayrı çıktı dosyası üretilir.

#### EYP İçeriğini Ayıklama

Bu özellik uygulama arayüzünde yer almamakta olup bağlam menüsü üzerinden kullanılmaktadır.

Her ne kadar doğrudan UDF dosyalarıyla ilişkili olmasa da, günlük kullanımda faydalı olduğu düşünüldüğünden uygulamaya dahil edilmiştir.

UETS üzerinden gönderilen evraklarda yer alan ekleri tek tek indirmek yerine, EYP paketinin tamamı indirilebilir ve ardından sağ tık menüsündeki **"EYP İçeriğini Ayıkla"** seçeneği kullanılarak paket içeriği çıkarılabilir. Bu özellik birden fazla EYP paketinin aynı anda işlenmesini destekler. Her arşiv için ayrı klasör oluşturulur.

Ayıklama işlemi sonucunda, EYP dosyasıyla aynı adı taşıyan bir klasör oluşturulur ve tüm ek dosyalar bu klasöre yerleştirilir.

## 3. Kullanım

Uygulamanın sol bölümünde dikey olarak sıralanmış sekmeler bulunmaktadır.

Üst bölümde:

* UDF'ye Dönüştür
* PDF'ye Dönüştür

sekmeleri yer alırken, orta bölümde:

* Tek Belge
* Çoklu Belge

sekmeleri bulunmaktadır.

Alt bölümde ise:

* Ayarlar
* Kullanım

sekmeleri yer almaktadır.

### Dönüştürme İşlemleri

Dönüştürme sekmelerinde:

1. Dosya veya dosyalar eklenir.
2. İstenirse çıktı klasörü seçilir.
3. Çıktının kaynak klasöre oluşturulması isteniyorsa herhangi bir klasör seçilmez.
4. Başlat düğmesine basılarak işlem tamamlanır.

### Çoğaltma İşlemleri

Çoğalt sekmelerinde:

1. Dosya veya dosyalar seçilir.
2. Değiştirilecek metin belirlenir.
3. Yeni değer veya değerler girilir.
4. İşlem başlatılır.

### Dosya Ekleme

Tek Belge sekmesi dışında tüm bölümler çoklu dosya eklemeyi desteklemektedir.

Dosyalar;

* Dosya ekleme düğmesi kullanılarak,
* Sürükle ve bırak yöntemiyle

uygulamaya eklenebilir.

### Kısayollar

Sekmeler arasında gezinme, işlem başlatma ve diğer klavye kısayolları **Kullanım** sekmesinde listelenmektedir.

### Ayarlar

Ayarlar sekmesinde aşağıdaki seçenekler bulunmaktadır:

* Uygulama teması
* Windows bağlam menüsü entegrasyonu

## 4. Proje Hakkında

UDF# herhangi bir ticari amaç güdülmeden geliştirilmiştir. Projenin temel amacı, günlük kullanım sırasında karşılaşılan bazı sorunlara çözüm üretmek ve zaman alan işlemleri daha verimli hâle getirmektir.

Uygulama büyük ölçüde yapay zekâ destekli araçlardan yararlanılarak geliştirilmiştir. Projenin özgün bir teknik yenilik veya akademik katkı sunduğu düşünülmediğinden kaynak kodları açık kaynak olarak yayımlanmamıştır.

GitHub deposu öncelikli olarak sürüm yönetimi, dağıtım ve yedekleme amacıyla kullanılmaktadır.

## 5. Sorumluluk Reddi

UDF#, geliştiricinin kendi ihtiyaçları doğrultusunda oluşturduğu ve zaman içerisinde geliştirdiği bir yardımcı araçtır. Uygulama mümkün olduğunca güvenilir ve kararlı çalışacak şekilde tasarlansa da, dönüştürme veya belge işleme süreçlerinde oluşabilecek veri kayıpları, biçimlendirme farklılıkları veya beklenmeyen sonuçlar konusunda herhangi bir garanti verilmemektedir.

Özellikle önemli belgeler üzerinde işlem yapılmadan önce ilgili dosyaların yedeklerinin alınması tavsiye edilir. Kullanıcılar, uygulamayı kullanarak gerçekleştirdikleri işlemlerin sonuçlarını kontrol etmekten kendileri sorumludur.


# Diğer Uygulamalar

* **UDF+**: Android için UDF, PDF ve TIFF görüntüleme, EYP açma; Word belgelerinden UDF'ye dönüştürme özelliklerini sunan kapsamlı bir UDF  görüntüleyici.
* Google Play Store: <https://play.google.com/store/apps/details?id=com.audivis.udfviewer>
* **AudiVis Player**: Android için erişilebilirlik odaklı, altyazı seslendirme özelliğine sahip video oynatıcı..
* Google Play Store: <https://play.google.com/store/apps/details?id=com.audivis.player>
