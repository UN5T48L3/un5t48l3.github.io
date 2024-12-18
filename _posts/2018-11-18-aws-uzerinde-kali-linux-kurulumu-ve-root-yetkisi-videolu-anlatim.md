---
title: 'AWS Üzerinde Kali Linux Kurulumu ve Root Yetkisi (Videolu Anlatım)'
date: '2018-11-18T22:31:36+03:00'
author: author1_id
layout: post
permalink: /aws-uzerinde-kali-linux-kurulumu-ve-root-yetkisi-videolu-anlatim/
image: /assets/img/kalioncloud.jpg
categories:
    - aws
tags:
    - 'amazon free tier'
    - 'amazon web services'
    - aws
    - 'aws free tier'
    - ec2
    - 'kali linux kurulumu'
    - 'kali linux nasıl kurulur'
    - 'kali linux on cloud'
    - 'kali linux root yetkisi'
    - 'kali on aws'
    - 'kali on cloud'
    - 'key pair'
format: video
---

> Kali Linux debian tabanlı, penetrasyon odaklı bir linux dağıtımıdır. Her PenTester için olmazsa olmazlardandır. Bu yazıda sizlere bulut üzerinde Kali Linux’u tamamen **ÜCRETSİZ** olarak kurup root yetkisiyle nasıl bağlanabileceğinizi anlatacağım.
> 
> <div class="jetpack-video-wrapper"><iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" frameborder="0" height="506" src="https://www.youtube.com/embed/tEYI8NnbpQY?feature=oembed" title="Kali Linux'u AWS Bulut Üzerinde Kurmak ve Root Yetkisi İle Bağlanmak" width="900"></iframe></div>

---

#### HAZIRLIK

Bulut servis sağlayıcılarını arasında en çok tercih edilen servislerden birisi şüphesiz ki AWS (Amazon Internet Companies)’dir. Biz de bugün AWS kullanarak Kali Linux işletim sistemimizi kolayca kuracağız. Öncelikle ihtiyacımız olan şeyler şunlardır;

- Temel Linux bilgisi
- Geçerli bir kredi kartı

#### Hadi başlayalım!

Şimdi [AWS Free Tier](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/?s=aws+free+tier) hesabımızı oluşturmak için bu adrese gidelim; [https://aws.amazon.com/tr/free/](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/free)

Üyeliğinizi tamamlayabilmek için içerisinde 5₺ civarında para olan bir kredi kartı ile kayıt olmanız gerekiyor. Ayrıca geçerli bir GSM numarası da gerekiyor. Amazon gibi kuruluşlar güvenlik sebebiyle bu gibi kampanyalarda kötü niyetlileri engelleyebilmek için üyelik aşamasında kredi kartından $1 USD çekip hemen geri yolluyorlar.

#### Artık Hazırız…

AWS konsolda [EC2](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/?s=ec2) (Elastic Compute Cloud) menüsüne girdikten sonra **Launch Occasion** butonuna tıklayarak makinemizi hazırlayalım. Burada **dikkat** etmemiz gereken; tüm ayarlarda **Free Tier** olanları seçmek. Aksi takdirde istemediğiniz faturalarla karşılaşabilirsiniz!

#### Bağlantı

Sonunda sunucumuza bağlanabiliriz. Sunucuya bağlanmak için oluşturduğumuz **.pem** uzantılı key pair’imiz gerekecek. Video’da detaylı olarak anlattım.

Sunuya bağlanmak için önce key pair’inizin izinlerini **400** olarak değiştirin. Daha sonra sunucuya bağlanın.

```
chmod 400 /path/my-key-pair.pem

ssh -i /path/my-key-pair.pem ec2-user@SERVE-IP-ADRESI
```

#### **Sisteme Root Olarak Login Olmak**

Bildiğiniz gibi normalde Kali Linux default olarak bizlere root izniyle giriş yapma olanağı sağlıyor. Fakat Amazon servisi güvenlik önlemi amacıyla default olarak **ec2-user** olarak giriş yapılmasına izin veriyor. Fakat biz, penetrasyon testleri sırasında sürekli problemlerle karşılaşmamak ve her seferinde “**sudo -i**” yazarak root şifresini girerek zaman kaybetmek yerine bunu standart Kali Linux ayarlarına çevireceğiz.

Gerekli komutlar;

```
sudo -i
psswd 
nano /and so on/ssh/sshd_config
```

Bu dosyada aşağıdaki iki satırı kontrol edip her ikisinin de “**sure**” olup olmadığını kontrol edin, eğer değilse sure olarak düzeltin.

**PermitRootLogin sure**

**PasswordAuthentication sure**

Daha sonra CTRL + O ile kaydedip CTRL + X ile çıkalım.

```
service sshd restart
```

Yukarıdaki komut ile sshd yeniden başlatılacak. Şimdi **exit** komutu ile EC2 serverımızdan çıkış yapalım.

Buraya kadar herşey tamam. Bu aşamadan sonra sonra eğer Linux ve MacOS kullanıcısı iseniz benim gösterdiğim yolu kullanarak bir ssh anahtarı oluşturacaksınız. Eğer Winzoz kullanıyorsanız, “ki kullanmamanızı öneririm.” [PuTTy-Gen](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/puttygen) kullanarak nasıl ssh anahtarı oluşturulduğu [Burada](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/puttygen) anlatılıyor.

Şimdi oluşturduğumuz ssh anahtarını Kali serverımıza kopyalayalım. Bunu da şu komutla yapacaksınız;

```
ssh-copy-id -i ~/path/to/ssh_anahtariniz.pub root<span class=""><span class="">@SERVER-IP-ADRESI</span></span>
```

Bu aşamada yukarıda “passwd” komutu ile oluşturduğumuz Root şifresini girerek işlemi tamamlıyoruz.

Şimdi aşağıdaki komutla Kali serverımıza yeniden bağlanalım;

```
ssh -i /path/my-key-pair.pem root@SERVE-IP-ADRESI
```

Son olarak ssh ayarlarını güvenli düzeye getirelim ki ssh anahtarı olmayan hiç kimse server’a bağlanamasın.

Komut;

```
nano /and so on/ssh/sshd_config
```

İlgili satırları aşağıdaki gibi düzeltelim

**PermitRootLogin without-password**

**PasswordAuthentication no**

CTRL + O ile kaydedip CTRL + X ile çıkalım.

ve

```
service sshd restart
```

## Sonunda!

Artık [AWS](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/?s=AWS) bulut sunucularında çalışan, root erişimli ve güvenli bir [Kali Linux](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/?s=Kali+Linux) işletim sisteminiz var. Makinenizi yeniden başlatırsanız ip adresiniz değişir. Bu yüzden [Elastic ip](https://mehmetcanyildiz.com.tr/wp-content/uploads/2018/11/elastic-ip-addresses-eip.html) almanızı öneririm.

|  |
|---|

##### Not: Bu yazı un5t48l3.com tarafından yazılmış olup izinsiz kullanımı durumunda yasal süreç başlatılacaktır.