---
title: 'Kişisel VPN Kurmak: Güvenli ve Özgür İnternet'
date: '2021-08-28T02:54:00+03:00'
author: author1_id
layout: post
permalink: /kisisel-vpn-kurmak-guvenli-ve-ozgur-internet/
image: /assets/img/wireguardvpn.png
categories:
    - vpn
tags:
    - digitalocean
    - 'digitalocean 100$'
    - 'digitalocean kupon'
    - 'engellenemez vpn'
    - ipv6
    - 'ipv6 vpn'
    - 'kişisel vpn'
    - 'kişisel vpn kurma'
    - openvpn
    - 'sansürsüz internet'
    - vpn
    - 'vpn sunucusu kurma'
    - wireguard
---

Merhaba siber güvenlik meraklıları, bu blog yazımda size kendinize ait bir **[VPN](https://un5t48l3.com/?s=vpn)** sunucusunu birkaç adımda nasıl kurabileceğinizi göstereceğim.  
Daha önce de **Outline** isimli VPN istemcisi ile yine bir VPN kurulumu anlatmıştım, ilgili videoya [buradan](https://www.youtube.com/watch?v=PDk1vzdU9YA&t=3s) ulaşabilirsiniz. ona da ulaşabilirsiniz.  
Bugün size çok daha güvenli, hızlı ve stabil olarak çalışan WireGuard isimli VPN sunucusunu ve istemcisini kullanarak Digitalocean üzerinde kendimize ait bir VPN sunucusunu nasıl oluşturabileceğimizi anlatacağım. Üstelik bu kişisel VPN kurulumu için 1 GB Ram ve 1 CPU olan en ucuz paket (5$) fazlasıyla yeterli olacak. WireGuard hakkında daha fazla bilgi almak için [www.wireguard.com ](https://www.wireguard.com/)adresini ziyaret edebilirsiniz.

## Neden Kişisel VPN Sunucusu Kurmalıyım?

Bildiğiniz gibi artık VPN servisi sağlayan binlerce, belki yüzbinlerce firma var.

<figure class="wp-block-image alignwide size-large is-style-default">![buy vpn](https://mehmetcanyildiz.com.tr/wp-content/uploads/2020/10/buy-vpn.jpg)<figcaption>buy vpn</figcaption></figure>Benim tavsiyem bu tür VPN sağlayıcılarını asla kullanmamanızdır. Size “**gizlilik**” vadederken bütün gizliliğinizi elinizden alabilirler. Çünkü genelikle açık kaynak kodlu değiller ve aynı sunuculara sizinle birlikte binlerce farklı kişi bağlanıyor. Üstelik bu kişilerin ne derecede yetenekli hackerler olduğunu bilmiyorsunuz. Bunun ne boyutlarda güvenlik zaafiyetlerine sebep olabileceğini tecrübe ederek öğrenmenizi istemediğim için böyle bir içerik oluşturma ihtiyacı duydum.

İşte bu tip VPN firmaları bütün internet trafiğinizi analiz ediyor ve hassas bilgilerinizi farklı amaçlar için biriktirebiliyorlar. Bunun yanı sıra sizin haberiniz olmadan arkaplanda farklı websitelerin ziyaret edilmesi gibi birçok etik olmayan davranış sergileyen firmalar da var. Ayrıca kullandığınız VPN firması hacklenirse siz dahil tüm kullanıcıların bütün hassas bilgileri de kötü niyetli insanlar tarafından kullanılabilecek ve hiç istemeyeceğiniz sonuçlar doğurabilecektir. Daha önce **NordVPN** isimli firma hacklenmiş ve kendileri de kabul etmiştir  
Bkz: <https://techcrunch.com/2019/10/21/nordvpn-confirms-it-was-hacked/>  
Not: <sub><sup>**Amacımın hiçbir VPN firmasını karalamak değil, sadece kişisel siber güvenliğinizi daha iyi ve efektif olarak nasıl sağlayabileceğinizi göstermek olduğunu da belirtmek isterim.** </sup></sub>


Peki VPN Sunucumuzu Nasıl Kuracağız?

  
“Client” yani istemci kurulumuyla başlayalım: <https://www.wireguard.com/install/> bağlantısına tıklayarak işletim sisteminiz için uygun olan adımları izleyin.

Kişisel VPN kurulumunda kullanacağımız sunucunun network hızı ve kullandığı iletişim protokolü teknolojileri ne kadar iyi olursa o kadar kaliteli bir VPN bağlantısı elde edersiniz. Ben server olarak [Digitalocean](https://m.do.co/c/f684ff061b7f) kullanıyorum. Aylık 5$ gibi makul bir fiyata gayet hızlı, ipv6 özelliği olan uygun bir hizmet sağlaması ve bu alanda kendini ispatlamış olması tercihimin başlıca nedenleridir.

##### **VPN Server Kurulumu:**

1. Create butonuna basın
2. Ubuntu 18 işletim sistemini seçin
3. Bulunduğunuz bölgeye yakın bir datacenter seçin
4. Şifre oluşturun, (Ssh key kullanmanızı öneririm böylelikle sunucuya şifre ile giriş tamamen devre dışı bırakılacaktır. Bu da sizi brute force saldırılarından koruyacaktır.)
5. **Ipv6**’yı da etkilenleştirin ve sunucuyu oluşturun.
6. Sunucuya bağlanın

#### Sunucuya bağlandıktan sonra;

- <https://github.com/angristan/wireguard-install> adresinden kurulumu gerçekleştirin
- Oluşturulan config dosyasını kopyalayıp istemcinize ekleyerek işlemi tamamlayın.

<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper"><div class="jetpack-video-wrapper"><iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" frameborder="0" height="506" src="https://www.youtube.com/embed/t8OLA7HtXQ8?feature=oembed" title="Kişisel VPN Sunucusu Kurulumu: WireGuard + DigitalOcean (ÇOK BASİT!)" width="900"></iframe></div></div><figcaption>DigitalOcean ile WireGuard kullanarak kişisel vpn kurulumu</figcaption></figure>Gördüğünüz gibi kısa bir süre içerisinde hiçbir kodlama, komut vs. ile uğraşmadan kendimize ait güvenli ve engellenemez bir VPN server kurmuş olduk.

Dilerseniz [buradan](https://m.do.co/c/f684ff061b7f) referans linkime tıklayarak üye olabilir, 60 gün boyunca Digitalocean’da kullanabileceğiniz 100$ kredisini kazanabilirsiniz. 🖖🏼  
  
  
Eğer videoyu ve yazımı beğendiyseniz videoda like butonuna tıklamayı ve kanalıma abone olmayı unutmayın. Ayrıca Siber Güvenlik’e meraklı daha fazla insana ulaşmamı sağlamak için videolarımı veya blog yazılarımı paylaşırsanız çok sevinirim.