---
title: "IP Adresleme Mekanizması Nedir?"
date: 2026-03-05 15:00:00 +0300
categories: [Bilgisayar Ağı, Network, İnternet, IP Adresleme Mekanizması]
tags: [bilgisayar-ağı, network, internet, ağ, ip-adresi, ip-adresleme-mekanizması, ip-addressing-mechanism, ip-address, ipv4, ipv6, ip-adresi-sınıfları, özel-ip-adresleri, private-ip-address, localhost]
image:
    path: /assets/img/ip_adresleme_mekanizmasiBaslik.png
    alt: IP Addressing Mechanism
---

## IP Adresleme Mekanizması

TCP/IP bilgisayar ağları oluştururken, önce ağdaki her cihaza bir mantıksal adres (**IP Adresi**) atanmalıdır. Bu atama işlemine "**IP Adresi Mekanizması (IP Addressing Mechanism)**" denir. Bu IP adresi ağdaki bir cihaza atanmazsa, ağ içindeki veya dışındaki cihazlarla iletişim kuramaz.

**IP Adresi Nedir?**

IP adresi, cihazın ağ adresinin kimliğidir. Bağlantı işlemleri IP adresleri kullanılarak gerçekleştirilir. IP adresleri IPv4 ve IPv6 olarak ikiye ayrılır. Her iki tür IP adresine de örnek olarak aşağıdaki IP adresleri verilebilir:

**IPv4: 192.168.4.1**
**IPv6: 2001:0db8:85a3:0000:0000:8a2e:0370:7334**

**IP Adresinin Yapısı**

IP adresi 4 bayttan (32 bit) oluşur. Her bayt arasına bir nokta yerleştirilir ve ondalık gösterimle ifade edilebilir. Her bayt 8 bitten oluştuğundan, her baytın minimum değeri alabilmesi için 8 bitlik değerin "**0(sıfır)**" olması gerekir. Benzer şekilde maksimum değeri elde etmek için her bayt için 8 bitlik değer "**1**" olmalıdır. IP adresinin her baytı "**0-255**" arasında bir değer alabilir.

**IP Adresi Sınıfları**

IP adresleri 5 sınıfa ayrılır. IP adresinin sınıfını öğrenmek için IP adresinin ilk baytı kontrol edilir. İlk baytın ondalık değerine göre, IP adresinin hangi sınıfa ait olduğu anlaşılır.

![ip-adresi-sınıflar](assets/ip-adresleme/ip-adresi-siniflari.png)

Bir IP adresine sahip cihazın hangi ağa dahil edildiğini IP adresi aracılığıyla bulmak mümkündür. Bu bilgiyi öğrenmek için öncelikle IP adresinin hangi sınıfa ait olduğu bilinmelidir.

![ornek-ip](assets/ip-adresleme/ornek-ip.png)

Aynı ilk 3 bayta sahip IP adreslerinin aynı ağdaki cihazlara ait olduğu söylenebilir. Örneğin "**192.168.4.1**" ve "**192.168.4.2**" aynı ağdadır. Çünkü yalnızca host bitlerinin bulunduğu baytta bir değişiklik vardır. Ağ bitleri aynı değere sahiptir.

![ornek-ip-adresi-sinif](assets/ip-adresleme/ornek-ip-sinif.png)

**IPv6 Nedir?**

Bugün, internet ağına bağlı cihaz sayısı oldukça yüksektir. Tüm bu cihazların bir IP adresine sahip olduğu düşünüldüğünde, IPv4 artık yeterli değildir. Bu nedenle bu sorunu çözmek için bazı teknolojiler (**NAT**) ve **IPv6** geliştirilmiştir. IPv6 ile sınırlı sayıda adrese sahip olan IPv4 kullanımı azalmaya başladı ve yerini IPv6'ya bıraktı. IPv6, 128 bitlik bir sayıdır.

**Özel(Private) IP Adresleri**

Bazı IP adresleri özel amaçlar için ayrılmıştır. Bu ayrılmış IP adresleri, özel ağlarda kullanılan IP adresleridir. Özel ağlar, doğrudan internete bağlı olmayan ve internete bir aracı ağ cihazıyla bağlanan ağlardır. Örneğin, ev ağları ve şirket içi ağlar. Ev içi ağlar, modem cihazı internete bağlantı sağlar ve paket akışını yönetir. Modem cihazı, ev ağına bakan bir ağ arayüzüne ve internet tarafına bakan bir ağ arayüzüne sahiptir. Özel ağ adı veilen kısım, modem cihazının ev ağ arayüzünün bulunduğu kısımdır. Bu bölümdeki cihazların IP adresleri, internet ortamında kullanılmayan ayrılmış IP adresleridir. Aşağıdaki görselde özel IP adresi aralıkları verilmiştir.

![ozel-ip-adresleri](assets/ip-adresleme/ozel-ip-adresleri.png)

**Localhost Nedir?**

Cihazın kendi ağ adresini belirten IP adresi aralığıdır. Cihazda yerel olarak çalışan hizmetlere erişmek için kullanılır. Yaygın olarak "**127.0.0.1**" IP adresi olarak bilinir. Ancak bu amaçla "**127.0.0.1-127.255.255.255**" aralığındaki herhangi bir IP adresi kullanılabilir. Başka bir ismi de geri döngü yani "**loopback**" adresidir.