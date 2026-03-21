---
title: "Temel Kavramlar"
date: 2026-03-06 16:30:00 +0300
categories: [Bilgisayar Ağı, Network, İnternet, Temel Kavramlar]
tags: [bilgisayar-ağı, network, internet, temel-kavramlar, basic-concepts, unicast, multicast, broadcast, broadcast-domain, collision-domain, subnet-mask, tek-noktaya-yayın, çoklu-yayın, yayın, yayın-alanı, çarpışma-alanı, alt-ağ-maskesi]
image:
    path: /assets/img/nat_Baslik.jpeg
    alt: IP Addressing Mechanism
---

## Temel Kavramlar

**Unicast (Tek Noktaya Yayın)**

**Unicast**, ağ paketlerini ağdaki tek bir hedefe iletmektir. Tek bir sistem ağ paketlerini tek bir hedefe iletirse buna **Unicast** denir.

![unicast](assets/temel-kavramlar/unicast.png)

**Multicast (Çoklu Yayın)**

**Multicast**, ağ paketlerinin aynı ağ içindeki birden fazla hedefe iletilmesidir.

![multicast](assets/temel-kavramlar/multicast.png)

**Broadcast (Yayın)**

**Broadcast**, ağdaki bir cihazın ağ paketlerini ağdaki tüm cihazlara iletmesidir.

![broadcast](assets/temel-kavramlar/broadcast.png)

**Broadcast Domain (Yayın Alanı)**

Genellikle yönlendiriciler tarafından ayrılmış her bir ayrı ağı ifade eder. **Yayın alanları**, yayın mesajlarının ulaşabileceği alanları ifade eder. Switchler, yayın alanlarını belirtmek için bazı yapılandırmalarla da kullanabilir.

![broadcast-domain]({{ site.baseurl }}/assets/temel-kavramlar/broadcast-domain.gif)

**Collision Domain (Çarpışma Alanı)**

Genellikle yayın etki alanlarından çok daha küçük alanlardır. **Çarpışma alanları**, aynı veri yolunu kullanarak paketler arasında çarpışmalara neden olabilecek alanlardır. Örneğin, Hub'ın bir bağlantı noktasından gelen paketler diğer tüm bağlantı noktalarına gönderildiğinden, Hub cihazının tüm bağlantı noktaları bir bütün olarak bir çarpışma alanı oluşturur. Öte yandan Switchler biraz farklıdır. Switchler hedef odaklı paketler ilettiğinden, Switchlerin her portu ayrı bir çarpışma alanı oluşturur.

![collision-domain]({{ site.baseurl }}/assets/temel-kavramlar/collision-domain.gif)

**Subnet Mask (Alt Ağ Maskesi) Nedir?**

**Subnet Mask (Alt Ağ Maskesi)**, ağ adreslerini tespit etmek ve ağları alt ağlara ayırmak için kullanılan bir adrestir. Ağ alt ağ maskesindeki her cihaza IP adresi atarken, cihazlar alt ağ maskesi olmadan ağ adreslerini bulamadığı için atama da yapılmalıdır. Ağ adresi bulunmazsa paket iletmede mümkün değildir. Kısacası, cihazlar arasında iletişim kurulamaz. Alt ağ maskesi, tıpkı IPv4 adresi gibi 4 bayt uzunluğundadır ve ondalık gösterimde ifade edilir.

**Örnek Alt Ağ Maskesi: 255.255.255.0**

**Varsayılan Alt Ağ Maskeleri**

Alt ağ maskeleri, her IP adresi sınıfı için varsayılan bir değere sahiptir.

![prefix-form](assets/temel-kavramlar/prefix-form.png)

Yukarıdaki bilgiler, her IP adresi sınıfı için varsayılan alt ağ maskelerini göstermektedir. Alt ağ maskelerinin bir başka temsili de "**Önek (Prefix)**" gösterimidir. Önek gösteriminde, alt ağ maskesindeki "**1**" bit sayısı belirtilir. Bu "**1**" bitler soldan sağa doğru sıradadır. Önek notasyonunda, bit sayısı "**/**" işareti ile yazılır. Örneğin, "**/8**" alt ağ maskesinin ikili gösterimi aşağıdaki gibidir.

**/8 = 11111111.00000000.00000000.00000000**

Bu örnekte, alt ağ maskesini temsil eden 32 bitin solundaki 8 bit "**1**" bitini gösterir ve kalan tüm bitler "**0**" bitini gösterir.

Tüm alt ağ maskeleri ve önek temsilleri aşağıdaki tabloda gösterilmiştir:

![tum-onek](assets/temel-kavramlar/tum-onek-temsilleri.png)

**Bitwise AND İşlemi**

AND, bitler üzerinde gerçekleştirilen işlemlerden biridir. Bitler üzerindeki AND işlemlerinin sonuçları aşağıda gösterilmiştir:

![bitwise](assets/temel-kavramlar/bitwise.png)