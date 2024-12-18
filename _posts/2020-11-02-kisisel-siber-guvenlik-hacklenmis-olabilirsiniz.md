---
title: 'Kişisel Siber Güvenlik Tavsiyeleri: Hacklendiğinizin Farkında Olmayabilirsiniz'
date: '2020-11-02T19:43:10+03:00'
author: author1_id
layout: post
permalink: /kisisel-siber-guvenlik-hacklenmis-olabilirsiniz/
image: /assets/img/kisiselsiberguvenlik.jpg
categories:
    - genel
tags:
    - 2fa
    - 'bilgisayar korsanı'
    - hacker
    - 'kişisel siber güvenlik'
    - linux
    - 'siber güvenlik'
    - 'siber savaş'
    - 'şifre güvenliği'
    - 'türkçe siber güvenlik'
---

Merhaba arkadaşlar, kişisel siber güvenlik tavsiyeleri verme ihtiyacı duymamın en önemli sebeplerinden biri son zamanlarda artan siber saldırılar. Yıllardır benim öngörüm siber savaşların yaklaştığı yönündeydi ve önümüzdeki 10 yıl içerisinde de çok ağır siber savaşlar yaşanacağını hep birlikte göreceğiz. Aslında siber savaşlar zaten başladı ama yakında çok daha fazla ses getirmeye başlayacak. Bunun sebebi ise artık hayatımızın tam ortasında “internet” diye bir şeyin var olması. İnternet sayesinde neredeyse aylarca evden çıkmadan da yaşanılabileceğini COVID-19 salgınında girdiğimiz karantinalarda görmüş olduk.

Gelelim siber savaşlara;  
Bu siber savaşlarda büyük hackerlar veya hacker grupları çarpışırken arada maalesef gerçek savaşlarda olduğu gibi masum veya hedef dışındaki insanlar da zarar görüyor/görecek, bu konuya birazdan değineceğim. Bu yüzden “Siber Güvenlik”, artık herkes için zaruri bir meseledir.

Bu yazımda maddeler halinde kendi siber güvenliğinizi nasıl sağlayabileceğinizden bahsedeceğim. Öncelikle şunu unutmayın, **HİÇBİR SİSTEM GÜVENLİ DEĞİLDİR**. Bizler sadece güvenlik için ek katmanlar oluşturuyoruz, çok iyi bir hacker gelip o güvenliği aşıyor ve biz yeni bir güvenlik sistemi geliştiriyoruz. İnternet ve teknoloji de bu şekilde gelişiyor zaten. Eğer karşınızdaki saldırgan hacker sizi hedef olarak seçmişse ve ne yaptığını gerçekten bilen bir hacker ise muhtemelen bu katmanların çoğunu rahatlıkla aşabilecektir. O zaman da profesyonel bir yardıma ihtiyacınız olabilir. Az önce bahsettiğim siber savaşlarda hedefte olmayanlar da zarar görebilir konusuna gelirsek;

Şöyle düşünün;  
Bir alışveriş sitesinin veritabanı saldırgan hacker tarafından ele geçiriliyor ve buradaki bütün kişisel bilgiler kullanılarak farklı “phishing” (oltalama) operasyonları yapılıyor. Ele geçirilen veritabanındaki bütün e-posta adreslerine gelişmiş yöntemleri ve aynı zamanda ele geçirilmiş veritabanındaki özel ve kişisel bilgileri kullanarak sizin tıklayabileceğiniz e-postalar veya kısa mesajlar yollanıyor. İşte bu siber savaşın bir parçası ve saldırganın asıl hedefi siz değilsiniz. Saldırgan burada tıpkı denize ağ atan balıkçılar gibi “ne denk gelirse” diye bu mailleri yolluyor ve maalesef mutlaka bunlara inanan ve bu yüzden birçok hesabını/parasını/özel verilerini çaldıran insanlar oluyor.

Ayrıca bazı e-postalar ile Ransomware dediğimiz fidye yazılımları da yayılıyor. Bu yazılım bulaştığı zaman cihazı (telefon veya bilgisayar) tamamen kilitliyor ve içerisindeki bütün sistemi şifreliyor. Böylece sistemdeki hiçbir veri okunamaz oluyor. Sisteminizi kurtarmak için de saldırganın belirtmiş olduğu kripto para adresine istediği miktarı yollamanız gerekiyor. Aksi takdirde hesabınızdaki verileri kaybediyorsunuz. En azından, o Ransomware için bir decrypter (şifre çözücü) geliştirilene kadar…

Peki, saldırgan sizin bilgilerinizi veya hesaplarınızı ele geçirip ne yapacak? Yapabileceği çok şey var. Eğer banka hesabınızı çalarsa yapacağı şey çok açık. Twitter, Facebook, Instagram hesabınızı çaldırdığınızda da hesabınız bir zombiye dönüşüyor, yani saldırgan bütün çaldığı hesaplardan aynı anda istediği gönderileri yolluyor ve bu şekilde isteklerini takipçilerinizin de görmesini sağlıyor. Bunu reklam olarak kullanlar da bir havuzda toplayıp oradan takipçi, beğeni vs. satanlar da var. Hatta ele geçirdiği hesapların içindeki bilgiler çok önemliyse bunları deepweb’de satabilirler. Kısacası bu işi meslek haline getirmiş ve gerçekten çok tehlikeli olan hackerlar var. Ben de böyle bir yazı yazarak tanıdığım/tanımadığım herkesin siber güvenlik hakkında bir nebze de olsa kafasındaki soru işaretlerini gidermek istedim. Bu kadar uzun bir metni ilk kez kaleme aldığım için hatalarım ve eksiklerim olabilir; affınıza sığınıyorum.

## **Peki Kendimi Bilgisayar Korsanlarından Nasıl Korurum?** 

“Tam olarak güvenlik” hiçbir zaman mümkün değildir. Zaten teknolojinin bu kadar hızlı ilerlemesinin sebebi de tam olarak bu. Siyah şapkalı hacker ve beyaz şapkalı hacker kavramları bu noktada karşımıza çıkıyor. Kötü niyetli bir bilgisayar korsanı, bir sisteme zarar veriyor veya bilgileri çalıyor. Buna karşı aynı veya daha fazla bilgi ve tecrübeye sahip başka bir bilgisayar korsanı da bu saldırılara karşı önlem almanın yöntemlerini geliştiriyor ve/veya siyah şapkalı hackerları takip ederek onların kimliğini tespit etmeye çalışıyor ve bu sonsuz bir döngü olarak devam ediyor. Beyaz şapkalı (white hat) hackerlar genellikle etik hacker (ethical hacker) olarak da anılmaktadır. Bana göre bu ayrımı her şey için yapabilirsiniz. Sadece siber güvenlik için böyle bir ayrım yapılmasının sebebi sanal dünyada iyi niyetli veya kötü niyetli insanları ayıran özelliklerin çok daha net olmasıdır. İyi ve kötü sadece bu alanda değil, dünyanın her yerinde var. Önemli olan vicdan sahibi olmak. Eğer vicdanlıysanız zaten normal hayatınızda da çevrenize zarar vermezsiniz.

Aşağıda bahsedeceğim birkaç madde ile kendinizi birçok siber saldırıdan (en azından amatör saldırılardan) koruyabilirsiniz.

### **Web tarayıcısı kişisel siber güvenliğinizin en önemli parçalarından birisi.**

1. SSL Sertifikası
    - Kullanmış olduğunuz tarayıcıdaki adres çubuğunda “**Güvenli Değil**” diye bir ibare görürseniz o siteden uzaklaşmanızı tavsiye ederim. Örnek: **http://siteadresi.com** yerine **https://siteadresi.com** olması gerekir.
2. Tarayıcınızda kullandığınız eklentilere de dikkat etmeniz gerekiyor. Ne olduğunu bilmediğiniz eklentiler varsa kaldırmanızda fayda var.
3. İnternette gezerken karşınıza çıkan uyarılardaki “izin ver” butonuna hemen tıklamayın, son zamanlarda neredeyse bütün siteler “push notifications” yollamak için izin istiyor.
    - Ben şahsen bütün bildirim izinlerini reddediyorum. Tıpkı mail adreslerimizi dağıttıkları veya sürekli reklam mailleri attıkları gibi bu özelliği de muhtemelen suistimal edecekler.
    - Ayrıca son zamanlarda bu özelliği phishing siteleri de kötüye kullanmaya başladı. Dikkatli olmak gerekir.

### **VPN: Kişisel siber güvenlik için olmazsa olmaz.** 

2. Çünkü aylık 5$ gibi fiyatlara 1 cpu vps alıp oraya openvpn veya wireguard gibi vpn cllientlarını kurabilirsiniz. Böylece bağlı olduğunuz vpn serverı üzerinden sadece sizin izin verdiğiniz cihazlar erişebilir. Nordvpn, Express vpn gibi uygulamaların bütün internet trafiğinizi analiz ettiğine ve verilerinizi sızdırdığına emin olabilirsiniz. Ayrıca aynı ağa yüzlerce kişi birden bağlı olduğu için neredeyse bütün VPN firmalarında ciddi hız düşüşü yaşarsınız. Kişisel siber güvenlik için DigitalOcean, AWS, GCP gibi yerlerde **VPN** kurduğunuz zaman hızınızda neredeyse hiçbir kayıp yaşamazsınız, sebebi de bu gibi firmaların çok fazla datacenter’a sahip olması ve sunucularının en son sistemleri ve teknolojileri kullanması.

### **Gelen mesajlara ve e-postalara çok dikkat edin. Phishing devam ediyor!**

1. Kısacası inanabileceğiniz derecede gerçekçi ama sahte e-posta ve websiteleriyle verilerin çalınması yöntemine oltalama diyoruz.
    - En çok kullanılan yöntemlerden birisi hâlâ **phishing**.

### **Kişisel siber güvenliğin en önemli parçalarından biri: Şifre güvenliği.** 

1. Şifrelerinizi unutmamak için bir yere kaydetmeyin, bir kağıda yazın veya internetle bağlantısı olmayan ayrı bir sistemde saklayın.
2. Şifrelerinizde büyük ve küçük harflerin yanı sıra rakam ve semboller kullanmanız şifrenizin bulunmasını zorlaştırır.
3. Aynı şifreyi birden fazla hesabınızda kullanmanız da risklidir.
4. Bir şekilde herhangi bir hesabınızın şifresi saldırgan tarafından ele geçirildiği anda aynı şifreyi kullandığınız bütün diğer hesaplarınızın da hacklenmesi kuvvetle muhtemeldir.

### **İki aşamalı doğrulamayı kullanın.** 

- Hesaplarınızın hepsinde **2FA** (iki aşamalı doğrulama) özelliğini aktifleştirin. Bunun için **Google Authenticator** uygulamasını kullanabilirsiniz.

### **Virüslerden korunun.**

1. Bildiğiniz gibi birçok antivirüs programı var fakat her antivirüs programı aynı derece güvenli değildir.
    - Ben linux sistemlerimde herhangi bir antivirüs kullanmıyorum. Firewall kurallarını düzgün ayarlarsanız ve çalışan uygulamaları düzenli olarak kontrol ederseniz Antivirüse pek ihtiyacınız olmaz.
2. Windows’a gelirsek; bence Microsoft Windows 10’u ilk çıkardığında rezalet bir durumdaydı, özellikle güvenliği aşırı düşüktü. Fakat şu an güvenliği bir tık artmış vaziyette.
    - Yine de Windows işletim sistemlerinde tavsiyem Eset firmasının çözümlerini kullanmanızdır. Kişisel tecrübelerime dayanarak söylüyorum; neredeyse bütün antivirüsleri bypass etmenin elbette farklı yöntemleri var fakat Eset bu alanda aşırı gelişmiş bir yapay zeka kullanıyor. Muhtemelen alanında çok iyi siber güvenlik uzmanlarıyla çalışıyor. Bu yüzden Antivirüs olarak Eset NOD32 benim için her zaman ilk sıradadır.

Bu yazımda hem teknik bilgisi olmayanların hem de siber güvenlik uzmanlarının rahatlıkla anlayabileceği şekilde kendi kişisel siber güvenliğinizi nasıl anlatmaya gayret ettim. Bu detayları herkesin mutlaka bilmesi gerektiği için değindim, tabii ki bir pentester olarak daha detaylı ve farklı yönlerine de sonraki yazılarımda değinebilirim. Amacım bu konularla pek ilgisi olmayan insanların kendi kişisel siber güvenliklerini nasıl sağlayabilecekleri hakkında fikir vermekti.

Lütfen görüşlerinizi yorumlarda belirtmeyi unutmayın. Profesyonel bir siber güvenlik asistanına ihtiyaç duyarsanız benimle iletişime geçebilirsiniz.