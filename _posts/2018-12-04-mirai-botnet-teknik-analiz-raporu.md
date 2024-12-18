---
title: 'Mirai Botnet Teknik Analiz Raporu'
date: '2018-12-04T15:02:41+03:00'
author: author1_id
layout: post
permalink: /mirai-botnet-teknik-analiz-raporu/
image: /assets/img/mirai-botnet.jpg
categories:
    - botnet
tags:
    - botnet
    - 'botnet saldırısı'
    - ddos
    - 'ddos saldırısı'
    - 'how to setup mirai'
    - 'internet of things'
    - iot
    - malware
    - mirai
    - 'mirai analiz'
    - 'mirai botnet nedir'
    - 'mirai tutorial'
    - 'ssh botnet'
    - 'telnet botnet'
---

**MIRAI Nedir ve Neden Bu Kadar Önemlidir?**

Mirai, DVR, IP kameralar, uydu alıcıları ve ev tipi yönlendiriciler gibi internete bağlı cihazları hedef alan bir zararlı yazılımdır. Özellikle bu cihazların zayıf güvenlik önlemleri nedeniyle, Mirai hem saldırıların etkisi hem de çalışma yöntemleriyle dikkat çeker. 21 Ekim 2016'da gerçekleşen saldırılar sonucunda en yaygın kullanılan internet servislerinde büyük kesintilere yol açarak dünya çapında gündem oldu.

### Mirai'nin Çalışma Prensibi ve Hedef Aldığı Zayıflıklar

Mirai, cihazların genellikle varsayılan kullanıcı adı ve parola ile kullanıldığını fark ederek bu zayıflıktan yararlanır. Kullanıcıların güvenlik bilinci eksikliği ve cihaz üreticilerinin yeterli güvenlik tedbirlerini sağlamaması, Mirai'nin geniş çaplı yayılmasını kolaylaştırır. Mirai, 61 adet zayıf ve standart kullanıcı adı/parola kombinasyonunu kendi içerisinde barındırarak, bu cihazları internette tarayıp ele geçirir.

**Hedef Aldığı Sistemler:**  
Mirai, Linux tabanlı işletim sistemlerini hedef alır ve ARM, MIPS, x86 gibi çeşitli işlemci mimarilerini destekler. Bu da onu geniş bir cihaz yelpazesi için tehdit haline getirir.

### Mirai Nasıl Yayılır?

Mirai'nin kaynak kodundaki *scanner.c* dosyası, yayılma yöntemleri hakkında detaylı bilgiler sunar:  

1. **Tarama İşlemi:**  
   Mirai, SYN Scan (Half Open Scan) kullanarak hızlı bir şekilde hedef sistemleri tarar. Rastgele IP adresleri oluşturur ve bu sırada özel ağ blokları ve ABD Savunma Bakanlığı gibi kritik IP alanlarını tarama dışı bırakır.  

2. **Hedefe Sızma:**  
   Ele geçirdiği sistemde, TELNET, SSH ve HTTP gibi hizmetleri durdurarak dış bağlantıları engeller. Ayrıca, sistemde başka bir Mirai örneği çalışıyorsa bunu tespit edip sonlandırır.

3. **Kendi Koruması:**  
   Mirai, çalıştığı dosya ve dizin adlarını bellekten silerek kendini tespit edilmekten korur. Ayrıca, QBOT veya ZOLLARD gibi diğer zararlıları bellek taramasıyla kapatır.

### Mirai'nin Saldırı Yöntemleri

Mirai, ele geçirdiği cihazları DDoS saldırıları için bir botnet ağına dönüştürür. Gerçekleştirebileceği saldırılar şunlardır:  

- **UDP Flood:** Ağ bant genişliğini tüketir.  
- **SYN Flood:** Bağlantı talepleriyle hedef sistemi doldurur.  
- **DNS Watertorture:** Hedefin DNS altyapısını zorlar.  
- **HTTP Flood:** Hedef web sunucusunu yoğun isteklerle yavaşlatır veya çökertir.  
- **ACK STOMP:** Yoğun ACK paketleriyle güvenlik duvarlarını aşar.  

### Mirai'ye Karşı Alınabilecek Önlemler

1. **Cihaz Envanteri:**  
   Ağınıza bağlı cihazların listesini çıkarın ve internete doğrudan erişimlerini engelleyin.  

2. **Uzaktan Yönetim:**  
   Uzaktan erişim portlarını kapatın veya standart portları değiştirin.  

3. **Güvenli Protokoller:**  
   TELNET yerine HTTPS ve SSH protokollerini kullanın.  

4. **Parola Güvenliği:**  
   Cihazların varsayılan parolalarını mutlaka değiştirin.  

5. **Ağ Trafiği Kontrolü:**  
   Kurumsal ağlarda dışa açık TELNET trafiğini engelleyin ve içeriye gelen ağ bağlantılarını düzenli olarak gözden geçirin.

### Sonuç

Mirai, nesnelerin interneti (IoT) cihazlarındaki güvenlik açıklarının ne kadar tehlikeli olabileceğini gösteren bir uyarıdır. Gerek bireysel kullanıcılar gerekse kurumlar için güvenlik önlemleri almak, Mirai gibi zararlı yazılımların etkisini en aza indirmede kritik bir role sahiptir. Bu olay, güvenlik bilincinin artırılması ve cihazların üretim aşamasında daha güvenli hale getirilmesi gerektiğini bir kez daha gözler önüne sermektedir.