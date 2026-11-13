ANOR ROBOTICS – BIOBUZZ | KURULUM REHBERİ

1) SİTEYİ ÖNİZLE
   ZIP'i çıkar. Terminal'de bu klasöre girip python3 -m http.server 8000 komutunu çalıştır.
   http://localhost:8000 adresine git. index.html dosyasını doğrudan çift tıklama: JSON fetch nedeniyle yerel sunucu gerekir.

2) MEVCUT NETLIFY SİTENİ GÜNCELLE
   Netlify > anor-robotics > Deploys bölümüne bu klasörü yükle.
   Eski adres değişmez. Formların çalışması için Netlify Forms özelliğini kontrol et.

3) GERÇEK CMS'İ ETKİNLEŞTİR (GITHUB GEREKLİ)
   - GitHub'da özel (private) veya açık bir depo oluştur ve BU klasördeki dosyaları depoya yükle.
   - admin/config.yml dosyasındaki repo: satırını GITHUB_KULLANICI/DEPO_ADI ile değiştir.
   - Netlify > Project configuration > Build & deploy > Repository bölümünden GitHub deposunu bağla.
   - Decap CMS GitHub OAuth için güvenli OAuth aracı/sunucusu kur ve admin/config.yml içinde base_url ve auth_endpoint alanlarını yapılandır.
     GitHub OAuth istemci sırrını ASLA web sitesinin JS/HTML dosyalarına koyma.
   - OAuth yetkilendirmesi tamamlandıktan sonra https://anor-robotics.netlify.app/admin/ üzerinden GitHub ile giriş yap.
   - İçeriği kaydettiğinde Decap CMS GitHub'a commit yapar; Netlify bağlı depodan otomatik yeniden yayınlar.

ÖNEMLİ: Sadece ZIP yüklemek Decap CMS girişini çalıştırmaz. GitHub depo bağlantısı ve OAuth sunucusu gereklidir.
Admin paneli henüz canlı oturum açma ile test edilmedi. Bu iki adım kullanıcı hesabı gerektirdiği için kullanıcı tarafından tamamlanmalıdır.

4) İÇERİKLER
   content/site.json dosyası tüm sayfaların içerik kaynağıdır.
   admin/config.yml bu alanları Türkçe düzenleme formlarına bağlar.
   Öğrenci fotoğraf ve isimleri için gerekli izinleri al.
   Sponsor, ödül ve takım üyesi bilgileri uydurulmadı.

5) GÖRSELLER
   assets/ klasöründeki logolar, banner, GIF ve altı BIOBUZZ görseli korunmuştur.
   WebP sürümleri daha hızlı yüklenir. Yeni yüklenen medya assets/uploads içine kaydedilir.

6) FORM
   İletişim formu Netlify Forms ile uyumlu statik HTML formudur. Netlify projesinde form algılama ve kota durumunu kontrol et.
