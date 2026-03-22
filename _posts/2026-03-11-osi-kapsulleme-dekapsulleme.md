---
title: "Data Encapsulation and Decapsulation in the OSI Model"
date: 2026-03-11 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, protokol, protocol, kapsülleme, encapsulation, decapsulation, dekapsülasyon, pdu, osi-modeli, katman, layer, physical, fiziksel, data-link, veri-bağlantısı, ağ, transport, taşıma, session, oturum, presentation, sunum, application, uygulama, fddi, slip, x.25, token-ring, atm, frame-relay, hdlc, ppp, ethernet, ip, ipx, icmp, igmp, bgp, ospf, rip, tcp, udp, atp, rpc, netbios, sql, ascii, binary, ebcdic, gif, jpeg, tiff, html, mpeg, ftp, telnet, smtp]
image:
    path: /assets/img/encapsulation_decapsulation_Baslik.jpg
    alt: Data Encapsulation and Decapsulation
---

## OSI Modelinde Veri Akışı

OSI Modeli hiyerarşik ve katmanlı bir mimariye sahiptir. Veri akışı, OSI modelindeki katmanlar arasında belirli bir yönde hareket eder.

![veri-akışı](assets/osi-kapsulleme/osi-veri-akisi.png)

## OSI Modelinde Veri Kapsülleme ve Dekapsülasyon İşlemi

Katmanların bazı başlık bilgileri, alıcı tarafında ihtiyaç duyulduğu gibi OSI modelindeki veri akışı sırasında ham verilere eklenir. Uygulamada çıkan ham verilerin yanına her katman için başlık bilgisi ekleme işlemene "**Kapsülleme(Encapsulation)**" denir. Gönderen tarafında gerçekleşen bu sürecin tersi alıcı tarafında da gerçekleştirilir. Her katman için başlık bilgileri, uygulama katmanından fiziksel katmana kadar olan toplam verilere dahil edilebilir. Bu nedenle alıcı tarafında ters yönde (fiziksel katmandan uygulama katmanına), her katman kendi başlık bilgilerini alır ve sorumlu olduğu üst katmana iletir. Bu şekilde uygulama içinde ham veriler elde edilir ve işlenir. Bu işleme alıcı tarafında "**Dekapsülasyon(Decapsulation)**" denir.

![kapsülleme-dekapsülasyon](assets/osi-kapsulleme/osi-encapsulation-decapsulation.png)

**OSI Modelinde Protokol Veri Birimi (PDU)**

OSI modelindeki her katman, kapsülleme/dekapsülasyon sürecinde farklı bir veri setine sahiptir. Bu veri kümesi bazı katmanlar için özel adlara sahiptir.

![osi-pdu](assets/osi-kapsulleme/osi-pdu.png)

**OSI Katmanları**

OSI modelinde ayrı görevlere sahip toplam 7 katman vardır. Bu katmanlar arasında hiyerarşik bir düzen vardır. Her katman bir sonraki katmana hizmet eder.

1. **Physical Layer (Fiziksel Katman)**

Veri iletim görevini barındıran katmandır. Veriler dijital (bit 0 veya 1 olarak) veya analog sinyaller şeklinde iletilir. Fiziksel iletişim kanallarına örnek olarak bükümlü çift kablolar, koaksiyel kablolar, fiber optik kablolar ve kablosuz iletişim verilebilir. Fiziksel katmanın görevleri şunlardır:

* Gönderilen verilerin gönderen tarafından gönderildiği gibi alınmasını sağlamak.
* Kaynak ve hedef arasında mekanik ve elektriksel tanımlar yaparak veri hareketini başlatmak, sürdürmek ve sonuçlandırmak.
* Verilerin dijital veya analog sinyal biçiminde gönderilip gönderilmeyeceğine karar vermek.

2. **Data Link Layer (Veri Bağlantısı Katmanı)**

Fiziksel adreslemenin gerçekleştirildiği yerdir. "**FDDI, SLIP, X.25, ATM, Token Ring, Frame Relay, HDLC, PPP ve Ethernet**"" bu katmandaki veri iletiminde kullanılan protokollerden bazılarıdır. Veri bağlantısı katmanının görevleri şunlardır:

* Fiziksel adreslemeyi sağlamak. (ARP Protokolü ile)
* Hata kontrolünü sağlamak. (CRC ile)
* Fiziksel katmana erişimi sağlamak ve ağ birimleri kullanılarak gönderilecek verilerin hedefini belirlemek.
* Fiziksel adresler (MAC adresleri) kullanarak fiziksel bağlantılar arasında güvenilir veri iletimi sağlamak.

3. **Network Layer (Ağ Katmanı)**

Ağ katmanı mantıksal adreslemenin gerçekleştirildiği yerdir. Bu katman, önceki katmandan alınan verileri işler ve verileri üst katman olan taşıma katmanına iletir. "**IP, IPX, ICMP, IGMP, BGP, OSPF ve RIP**" bu katmanda kullanılan protokollerden bazılarıdır. Ağ katmanın işlevleri şunlardır:

* İki mantıksal düğüm arasında veri iletimini sağlamak.
* Her düğümü tanımlayan mantıksal adreslemeyi uygulamak.
* Farklı ağlardaki bilgisayarlar arasında veri iletimi sağlayan yönlendirme mekanizmasını tanımlamak.

4. **Transport Layer (Taşıma Katmanı)**

Taşıma katmanı, veri iletimi ve iletim güvenliğinden sorumlu olandır. Bu katman hata kontrolü için son OSI katmanıdır. "**TCP, UDP ve ATP**" bu katmanda kullanılan protokollerden bazılarıdır. Taşıma katmanının görevleri şunlardır:

* İki düğüm arasındaki iletimin akış kontrolü aracılığıyla her iki düğüm için uygun hızda olmasını sağlamak.
* Bozuk verileri tespit etmek ve hata kontrolü yoluyla iletilmesini önlemek.

5. **Session Layer (Oturum Katmanı)**

Bilgisayarlar arasındaki bağlantıların kurulumunun, yönetiminin ve sonlandırılmasının gerçekleştirildiği katmandır. Ek olarak, oturum katmanı protokollerdeki veri akışını kendi katmanında kontrol eder. "**RPC, SQL ve NetBIOS**" bu katmanda kullanılan protokollerden ve uygulamalardan bazılarıdır.

6. **Presentation Layer (Sunum Katmanı)**

Veri taramasının yapıldığı katmandır. "**ASCII, Binary ve EBCDIC**" veri görüntüleme türlerinden bazılarıdır. Bu katman, verilerin sıkıştırılmasından ve şifrelenmesinden de sorumlu olabilir. "**GIF, JPEG, TIFF, ASCII, HTML ve MPEG**" bu katmanda kullanılan veri formatlarından bazılarıdır.

7. **Application Layer (Uygulama Katmanı)**

Kullanıcıların önündeki uygulamaların işlendiği ilk katmandır. Uygulamadaki işlemler genellikle bu katmana dahil edilir. "**FTP, HTTP, TELNET ve SMTP**" bu katmanda kullanılan bazı protokollerdir.