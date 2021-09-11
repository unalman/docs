# Vue Dokümanlarının Yazım Kılavuzu

Belge yazmak bir empati alıştırmasıdır. Nesnel bir gerçekliği tanımlamıyoruz - kaynak kodu zaten bunu yapıyor. Bizim işimiz, kullanıcılar ve Vue ekosistemi arasındaki ilişkiyi şekillendirmeye yardımcı olmaktır. Bu sürekli gelişen kılavuz, Vue ekosisteminde bunun tutarlı bir şekilde nasıl yapılacağına dair bazı kurallar ve öneriler sunar.

## Prensipler

- **Bir özellik, iyi belgelenene kadar mevcut değildir.**
- **Kullanıcıların bilişsel kapasitesine (yani beyin gücüne) saygı gösterin.** Bir kullanıcı okumaya başladığında, belirli bir miktarda sınırlı beyin gücüyle başlar ve bittiğinde öğrenmeyi bırakır.
  - Bilişsel kapasite, karmaşık cümleler, aynı anda birden fazla kavram öğrenme zorunluluğu ve kullanıcının çalışmasıyla doğrudan ilgili olmayan soyut örnekler nedeniyle daha **hızlı tükenir**.
  - Sürekli olarak akıllı, güçlü ve meraklı hissetmelerine yardımcı olduğumuzda, bilişsel kapasite **daha yavaş tükenir**. İşleri sindirilebilir parçalara ayırmak ve dokümanın akışına dikkat etmek onları bu durumda tutmaya yardımcı olabilir.
- **Daima kullanıcının bakış açısından bakmaya çalışın.** Bir şeyi iyice anladığımızda, bizim için apaçık hale gelir. Buna _bilginin laneti_ denir. İyi dokümanlar yazmak için, bu kavramı öğrenirken ilk olarak bilmeniz gerekenleri hatırlamaya çalışın. Hangi jargonu öğrenmen gerekiyordu? Neyi yanlış anladın? Neyi gerçekten kavramak uzun zaman aldı? İyi dokümantasyon, kullanıcılarla bulundukları yerde buluşur. Konsepti insanlara daha önce yüz yüze açıklama alıştırması yapmak faydalı olabilir.
- **Önce _sorunu_, ardından çözümü tanımlayın.** Bir özelliğin nasıl çalıştığını göstermeden önce, neden var olduğunu açıklamak önemlidir. Aksi takdirde, kullanıcılar bu bilgilerin kendileri için önemli olup olmadığını (Yaşadıkları bir sorun mu?) veya hangi ön bilgiye/deneyime bağlanacağını bilecek içeriğe sahip olmayacaktır.
- **Yazarken soru sormaktan çekinmeyin**, özellikle de "aptalca" olabileceğinden korkuyorsanız. Kolay incinebilir olmak zordur, ancak açıklamamız gereken şeyi daha tam olarak anlamamızın tek yolu budur.
- **Özellik tartışmalarına katılın.** En iyi API'ler, daha sonra nasıl açıklanacağını bulmaya çalışmak yerine, açıklanması kolay özellikler oluşturduğumuz, dokümantasyona dayalı geliştirmeden(documentation-driven development) gelir. Soruları daha erken sormak (özellikle "aptalca" soruları), genellikle kafa karışıklıklarını, tutarsızlıkları ve sorunlu davranışları, bunları düzeltmek için bir kırılma değişikliği gerekmeden önce ortaya çıkarmaya yardımcı olur.

## Organizasyon

- **Kurulum/Entegrasyon**: Yazılımın gerektiği kadar çok farklı türdeki projeye nasıl entegre edileceğine dair kapsamlı bir genel bakış sağlayın.
- **Giriş/Başlarken**:
  - Projenin çözdüğü sorunlara ve neden var olduğuna dair 10 dakikadan daha kısa bir genel bakış sağlayın.
  - Projenin ne zaman ve neden kullanılacağı ve bazı basit kod örnekleri de dahil olmak üzere, projenin çözdüğü sorunlara ve nasıl olduğuna dair 30 dakikadan daha kısa bir genel bakış sağlayın. Sonunda, hem Kurulum sayfasına hem de Temel Bilgiler Kılavuzunun başlangıcına bağlantı verin.
- **Kılavuz**: Kullanıcıları akıllı, güçlü ve meraklı hissettirin, ardından bu durumu koruyun, böylece kullanıcılar daha fazla öğrenmeye devam etmek için motivasyon ve bilişsel kapasiteyi sürdürsün. Kılavuz sayfaları sırayla okunmak içindir, bu nedenle genellikle en yüksekten en düşük güç/efor oranına göre sıralanmalıdır.
  - **Temeller**: Temelleri okumak 5 saatten uzun sürmemelidir, ancak daha kısası daha iyidir. Amacı, kullanıcıların kullanım durumlarının %80'ini ele almasına yardımcı olacak bilginin %20'sini sağlamaktır. Temeller, daha gelişmiş kılavuzlara ve API'ye bağlantı verebilir, ancak çoğu durumda bu tür bağlantılardan kaçınmalısınız. Sağlandığında, kullanıcıların ilk okumalarında bu bağlantıyı izlemeleri gerekip gerekmediğini anlamaları için bir bağlam da sağlamanız gerekir. Aksi takdirde, birçok kullanıcı, devam etmeden önce bir özelliğin her yönünü tam olarak öğrenmeye çalışarak bilişsel kapasite bağlantı atlamasını tüketir ve sonuç olarak, Temellerin ilk okumasını asla bitirmez. Düzgün bir okumanın kapsamlı olmaktan daha önemli olduğunu unutmayın. İnsanlara sinir bozucu bir deneyim yaşamamaları için ihtiyaç duydukları bilgileri vermek istiyoruz, ancak her zaman geri dönüp daha fazla okuyabilirler veya Google'da daha az yaygın bir sorunla karşılaştıklarında.
  - **İleri Seviye**: Temeller, kullanıcıların kullanım durumlarının ~%80'ini ele almasına yardımcı olurken, sonraki kılavuzlar, kullanıcıların kullanım durumlarının %95'ine ulaşmasına yardımcı olur ve ayrıca temel olmayan özellikler (örneğin. geçişler, animasyonlar), daha karmaşık kolaylık özellikleri (örneğin. mixins, özel yönergeler) ve geliştirme deneyimi iyileştirmeleri hakkında daha ayrıntılı bilgiler sağlar. (örneğin. JSX, eklentiler). Daha niş, karmaşık ve/veya kötüye kullanıma açık kullanım durumlarının son %5'i, bu gelişmiş kılavuzlardan bağlantı kurulabilecek yemek kitabına ve API referansına bırakılacaktır.
- **Referans/API**: Tür bilgileri, her birinin çözdüğü sorunun açıklamaları, her seçenek kombinasyonunun örnekleri ve kılavuzlara, yemek kitabı tariflerine ve daha fazla ayrıntı sağlayan diğer dahili kaynaklara bağlantılar dahil olmak üzere özelliklerin tam bir listesini sağlayın. Diğer sayfalardan farklı olarak, bu sayfa yukarıdan aşağıya okunacak şekilde tasarlanmamıştır, bu nedenle bol miktarda ayrıntı sağlanabilir. Bu referanslar ayrıca kılavuzlardan daha kolay gözden geçirilebilir olmalıdır, bu nedenle format, kılavuzların hikaye anlatım formatından ziyade sözlük girişlerine daha yakın olmalıdır.
- **Göçler(Migrations)**:
  - **Versiyonlar**: Önemli değişiklikler yapıldığında, değişikliğin neden yapıldığına ve projelerinin nasıl taşınacağına ilişkin ayrıntılı bir açıklama da dahil olmak üzere, değişikliklerin tam listesini eklemek yararlıdır.
  - **Diğer projelerden**: Bu yazılım benzer yazılımlarla nasıl karşılaştırılır?Bu, kullanıcıların kendileri için hangi ek sorunları çözebileceğimizi veya yaratabileceğimizi ve zaten sahip oldukları bilgileri ne ölçüde aktarabileceklerini anlamalarına yardımcı olmak için önemlidir.
- **Stil rehberi**: Geliştirme aşamasında mutlaka karar verilmesi gereken ancak API'nin özü olmayan bazı önemli parçalar vardır. Stil kılavuzu, bu kararlara rehberlik etmeye yardımcı olmak için eğitimli, fikirli öneriler sunar. Körü körüne takip edilmemelidirler, ancak daha küçük ayrıntılar üzerinde hizalanarak ekiplerin zaman kazanmalarına yardımcı olabilir.
- **Yemek kitabı**: Yemek kitabındaki tarifler, Vue ve ekosistemine aşinalık varsayımıyla yazılmıştır. Her biri, bir Vue geliştiricisinin karşılaşabileceği bazı genel uygulama ayrıntılarını anlatan yüksek düzeyde yapılandırılmış bir belgedir.

## Yazım ve Dilbilgisi

### Stil

- **Başlıklar sorunları tanımlamalıdır**, çözümleri değil. Örneğin, daha az etkili bir başlık, bir çözümü tanımladığı için "prop'ları kullanma" olabilir. Daha iyi bir başlık "Prop'lar ile Alt Bileşenlere Veri Geçirme" olabilir, çünkü prop'ların çözdüğü sorunun bağlamını sağlar. Kullanıcılar, bir özelliği neden/ne zaman kullanacaklarına dair bir fikirleri olana kadar, bir özelliğin açıklamasına gerçekten dikkat etmeye başlamazlar.
- **Bilgiyi kabul ettiğinizde, bunu en baştan beyan edin** ve beklediğiniz daha az yaygın bilgi için kaynaklara bağlantı verin.
- **Mümkün olduğunca bir seferde yalnızca bir yeni konsept tanıtın** (hem metin hem de kod örnekleri dahil). Birden fazla konsept tanıttığınızda birçok kişi anlayabilse bile, kaybolacak birçok kişi de olacaktır - ve kaybolmayanlar bile bilişsel kapasitelerinin çoğunu tüketmiş olacaktır.
- **Mümkün olduğunca ipuçları ve uyarılar için özel içerik bloklarından kaçının.** Bunları ana içeriğe daha doğal bir şekilde karıştırmak genellikle tercih edilir, ör. Edge durumunu göstermek için örnekler üzerine inşa ederek.
- **Sayfa başına ikiden fazla iç içe geçmiş ipucu ve uyarı eklemeyin.** Bir sayfada ikiden fazla ipucunun gerekli olduğunu fark ederseniz, bu sorunları gidermek için bir uyarı bölümü eklemeyi düşünün. Kılavuzun doğrudan okunması amaçlanmıştır ve ipuçları ve uyarılar, temel kavramları anlamaya çalışan biri için bunaltıcı veya dikkat dağıtıcı olabilir.
- **Otoriteye başvurmaktan kaçının** (Örneğin. "X yapmalısın, çünkü bu en iyi uygulamadır" veya "X en iyisidir çünkü size endişeleri tam olarak ayırmanızı sağlar"). Bunun yerine, bir örüntü tarafından neden olunan ve/veya çözülen belirli insan sorunlarını örneklerle gösterin.
- **İlk önce neyi öğreteceğinize karar verirken, hangi bilginin en iyi güç/çaba oranını sağlayacağını düşünün.** Bu, kullanıcıların en büyük acıları veya en fazla sayıda sorunu çözmelerine yardımcı olacak her şeyi, nispeten daha az öğrenme çabasıyla öğretmek anlamına gelir. Bu, öğrencilerin kendilerini akıllı, güçlü ve meraklı hissetmelerine yardımcı olur, böylece bilişsel kapasiteleri daha yavaş tükenir.
- **Bağlamda bir string şablonu veya yapı sistemi olmadığı sürece, yalnızca yazılım tarafından herhangi bir ortamda çalışan kodu yazın (örn. Vue, Vuex, vb.).**
- **Göster, söyleme.** Örneğin, "Bir sayfada Vue kullanmak için, değeri Vue'nun derlenmiş kaynağına bir bağlantı olması gereken src niteliğine sahip bir komut dosyası öğesi ekleyebilirsiniz." yerine "Bir sayfada Vue kullanmak için bunu HTML'nize ekleyebilirsiniz" (ardından komut dosyası etiketini gösterin).
- **Neredeyse her zaman mizahtan kaçının (İngilizce dokümanlar için)**, özellikle alaycılıktan ve popüler kültür referanslarından kaçının, çünkü kültürler arasında iyi bir şekilde tercüme edilmez.
- **Asla olması gerekenden daha gelişmiş bir bağlam varsaymayın.**
- **Çoğu durumda, aynı içeriği birden çok bölümde tekrarlamak yerine, dokümanların bölümleri arasındaki bağlantıları tercih edin.** İçerikte bazı tekrarlar kaçınılmazdır ve hatta öğrenme için gereklidir. Bununla birlikte, çok fazla tekrar, dokümanların bakımını daha da zorlaştırır, çünkü API'deki bir değişiklik birçok yerde değişiklik yapılmasını gerektirir ve bir şeyleri gözden kaçırmak kolaydır.This is a difficult balance to strike.
- **Spesifik, genelden daha iyidir.** Örneğin, bir `<BlogPost>` bileşen örneği `<ComponentA>`'dan daha iyidir.
- **İlişkilendirilebilir, belirsiz olmaktan iyidir.** Örneğin, bir `<BlogPost>` bileşen örneği, `<CurrencyExchangeSettings>` öğesinden daha iyidir.
- **Duygusal olarak ilgili olun.** İnsanların deneyimlediği ve önemsediği bir şeyle ilgili açıklamalar ve örnekler her zaman daha etkili olacaktır.
- **Karmaşık veya jargonlu bir dil yerine her zaman daha basit, daha sade bir dil tercih edin.** Örneğin:
  - "Vue'yu bir komut dosyası öğesiyle kullanabilirsiniz" yerine "Vue kullanımını başlatmak için olası bir seçenek, onu bir komut dosyası HTML öğesi aracılığıyla gerçekten enjekte etmektir"
  - "yüksek dereceli fonksiyon" yerine "fonksiyon döndüren fonksiyon"
- **Çabalamayı geçersiz kılan dilden kaçının**, "kolay", "sadece", "belli ki" vb. Referans için bkz. [Eğitici Yazılarda Kaçınılması Gereken Sözler](https://css-tricks.com/words-avoid-educational-writing/).

### Gramer

- **Kısaltmalardan kaçının.** Bir API'de özel olarak bir kısaltmaya atıfta bulunmuyorsanız (örneğin, `$attrs`), yazma ve kod örneklerinde kısaltmalardan kaçının (örneğin, `attribute`, `attr`'dan daha iyidir, `message`, `msg`'den daha iyidir). Standart klavyelerde bulunan kısaltma sembolleri (ör. `@`, `#`, `&`) uygundur.
- **Doğrudan aşağıdaki örneğe atıfta bulunurken, cümleyi sonlandırmak için nokta (.) yerine iki nokta üst üste (:) kullanın.**
- **Oxford virgülünü kullanın** (örneğin "a, b ve c" yerine "a, b ve c"). ![Oxford virgülü neden önemlidir?](/images/oxford-comma.jpg)
  - Kaynak: [Seri (Oxford) Virgül: Ne Zaman ve Neden Kullanılmalı](https://www.inkonhand.com/2015/10/the-serial-oxford-comma-when-and-why-to-use-it/)
- **Bir projenin adına atıfta bulunurken, projenin kendisine atıfta bulunduğu adı kullanın.** Örneğin, "webpack" ve "npm", dokümantasyonlarında bunlara atıfta bulunduğu için küçük harf kullanmalıdır.
- **Başlıklar için Başlık Durumunu kullanın** - en azından şimdilik, çünkü dokümanların geri kalanında kullandığımız şey budur. Cümle durumunun (başlığın yalnızca ilk kelimesi büyük harfle başlar) aslında okunaklılık açısından üstün olduğunu ve ayrıca belge yazarları için bilişsel yükü azalttığını öne süren araştırmalar var, çünkü "ve", "ile" ve "hakkında" gibi sözcükleri büyük harf yapıp yapmadıklarını hatırlamaya çalışmak zorunda değiller.
- **Emoji kullanmayın (tartışmalar dışında).** Emojiler sevimli ve arkadaş canlısıdır, ancak belgelerde dikkat dağıtıcı olabilirler ve hatta bazı emojiler farklı kültürlerde farklı anlamlar taşır.

## Yineleme ve İletişim

- **Mükemmellik yinelemeden gelir.** İlk taslaklar her zaman kötüdür, ancak bunları yazmak sürecin hayati bir parçasıdır. Kötü -> Tamam -> İyi -> Harika -> İlham Veren -> Üstün yavaş ilerlemesinden kaçınmak son derece zordur.
- **Yayınlamadan önce yalnızca bir şeyin "İyi" olmasını bekleyin.** Topluluk, onu zincirde daha da aşağı itmenize yardımcı olacaktır.
- **Geri bildirim alırken savunmaya geçmemeye çalışın.** Yazımız bizim için çok kişisel olabilir, ancak daha iyi hale getirmemize yardımcı olan insanlara üzülürsek, ya geri bildirim vermeyi bırakırlar ya da verdikleri geri bildirim türünü sınırlamaya başlarlar.
- **Başkalarına göstermeden önce kendi çalışmanızın yazım hatalarını bulup düzeltin.** Birine çok sayıda yazım/dil bilgisi hatası olan bir çalışma gösterirseniz, yazının hedeflerinize ulaşıp ulaşmadığına ilişkin daha değerli notlar yerine yazım dilbilgisi/hataları hakkında geri bildirim alırsınız.
- **İnsanlardan geri bildirim istediğinizde, yorum yapacak olanlara şunları söyleyin:**
  - **yapmaya çalışıyorsun**
  - **senin korkuların**
  - **vurmaya çalıştığınız dengeler**
- **Birisi bir sorun bildirdiğinde, önerdiği çözüm tam olarak doğru olmasa bile hemen hemen her zaman bir sorun vardır.** Daha fazla bilgi edinmek için takip soruları sormaya devam edin.
- İnsanların içeriğe katkıda bulunurken/incelerken soru sorarken kendilerini güvende hissetmeleri gerekir. Bunu şu şekilde yapabilirsiniz:
  - **Huysuz olsanız bile insanlara katkıları/incelemeleri için teşekkür edin.** Örneğin:
    - "Harika soru!"
    - "Açıklamaya zaman ayırdığınız için teşekkürler. 🙂"
    - "Bu aslında kasıtlıdır, ancak zaman ayırıp katkıda bulunduğunuz için teşekkür ederiz. 😊"
  - **İnsanların söylediklerini dinleyin ve doğru anladığınızdan emin değilseniz yansıtın.** Bu, insanların duygularını ve deneyimlerini doğrulamaya yardımcı olurken aynı zamanda _onları_ doğru anlayıp anlamadığınızı da anlayabilir.
  - **Bol bol pozitif ve empatik emoji kullanın.** Biraz garip görünmek, kaba veya sabırsız olmaktan her zaman daha iyidir.
  - **Lütfen kuralları/sınırları iletin.** Birisi taciz edici/uygunsuz bir şekilde davranırsa, yalnızca nezaket ve olgunlukla yanıt verin, ancak aynı zamanda bu davranışın kabul edilemez olduğunu ve kötü davranmaya devam ederse (davranış kurallarına göre) ne olacağını açıkça belirtin.

### İpuçları, Açıklamalar, Uyarılar ve Öne Çıkanlar

Belirli bir şekilde vurgulanmaya değer bir şeyi belirtmek için bazı özel stillerimiz var. bunlar [bu sayfada](https://v3.vuejs.org/guide/doc-style-guide.html#alerts) ele alınır. **Az miktarda kullanılmalıdırlar.**

Bu stilleri kötüye kullanmak için belirli bir ayartma vardır, çünkü bir belirtme çizgisinin içine basitçe bir değişiklik eklenebilir. Ancak bu, kullanıcının okuma akışını bozar ve bu nedenle yalnızca özel durumlarda kullanılmalıdır. Mümkün olan her yerde, okuyucunun bilişsel yüküne saygı göstermek için sayfa içinde bir anlatı ve akış oluşturmaya çalışmalıyız.

Hiçbir koşulda 2 uyarı yan yana kullanılmamalıdır, bu, bağlamı yeterince iyi açıklayamadığımızın bir işaretidir.

### Katkı

Küçük, odaklanmış PR'ları takdir ediyoruz. Son derece büyük bir değişiklik yapmak istiyorsanız, lütfen bir pull request'den önce ekip üyeleriyle iletişim kurun. İşte bu ekipte iyi çalışmamızın [neden bu kadar kritik olduğunu ayrıntılarıyla anlatan bir yazı](https://www.netlify.com/blog/2020/03/31/how-to-scope-down-prs/). Lütfen katkıları her zaman takdir etmemize rağmen, sonuçta bir bütün olarak proje için en iyi olanı önceliklendirmemiz gerektiğini anlayın.

## Kaynaklar

### Yazılım

- [Grammarly](https://www.grammarly.com/): Yazım ve dil bilgisi denetimi için masaüstü uygulaması ve tarayıcı uzantısı (dilbilgisi denetimi her şeyi yakalamaz ve bazen yanlış bir pozitif gösterir).
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): markdown ve kod örnekleri içinde yazım denetimi yapmanıza yardımcı olacak bir VS Kodu uzantısı.

### Kitaplar

- [On Writing Well](https://www.amazon.com/Writing-Well-30th-Anniversary-Nonfiction-ebook/dp/B0090RVGW0) ([popüler alıntıları](https://www.goodreads.com/work/quotes/1139032-on-writing-well-the-classic-guide-to-writing-nonfiction) görün)
- [Bird by Bird](https://www.amazon.com/Bird-Some-Instructions-Writing-Life/dp/0385480016) ([popüler alıntıları](https://www.goodreads.com/work/quotes/841198-bird-by-bird-some-instructions-on-writing-and-life) görün)
- [Cognitive Load Theory](https://www.amazon.com/Cognitive-Explorations-Instructional-Performance-Technologies/dp/144198125X/)
