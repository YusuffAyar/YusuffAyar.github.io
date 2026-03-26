---
title: "Internet Control Message Protocol (ICMP)"
date: 2026-03-17 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, icmp, internet-kontrol-mesajı-protokolü, internet-control-message-protocol]
image:
    path: /assets/img/icmp_Baslik.png
    alt: Internet Control Message Protocol
---

## İnternet Kontrol Mesaj Protokolü (ICMP) Nedir?

ICMP, paketlerin gönderen cihaza iletilmesi sırasında hataları, uyarıları ve kontrol mesajlarını gönderen protokoldür.

**ICMP Protokolünün Özellikleri**

* IP protokolü ile çalışır.
* ICMP mesajları genellikle aşağıdaki durumlarda oluşturulur:

1. IP paketleri hedeflerine ulaşmadığında
2. Ağ geçidi cihazları paketleri iletmeyecek kadar meşgul olduğunda
3. Paketlerin gitmesi için daha kısa bir yol olduğunda

* ICMP protokolü IP protokolünü daha güvenli hale getirmez.
* IP protokolünü kullanan tüm uygulamalar ICMP protokolünü desteklemelidir.
* ICMP mesajlarının tümü hata kontrolü hakkında bilgi sağlamaz. Bazı ICMP mesajları bilgisayar ağı testlerini ve ağ bilgilerini elde etmek için kullanılır.
* ICMP protokolü yalnızca IP paketleri için hata mesajları üretir. ICMP protokolü, ICMP mesajlarının iletimiyle ilgili hatalar durumunda hata mesajları üretmez.
* ICMP mesajları, hata mesajlarını gösterseler bile hatayı düzeltmek için ne yapılması gerektiği hakkında bilgi içermez. Bu, hata mesajını alan bilgisayar tarafından belirlenen bir durumdur.

## ICMP Uygulamaları

1) **Ping**

Ping, ağdaki cihazın ICMP mesajları kullanılarak iletilip iletilmediğini öğrenmek için kullanılan bir uygulamadır. 

![ping-istegi](assets/icmp/ping-istegi.png)

ICMP ping isteği "**-c**" parametresine sahip "5" paketi ile gönderildi. Yanıt paketinin gönderilen pakete geri göndüğünü gördüğümüzde hedef adresle bir iletişimi vardır.

**NOT**: Bazı ağlarda, güvenlik açısından güvenlik duvarı yapılandırmaları aracılığıyla ICMP mesajları engellenir. Bu nedenle, böyle bir ağda ping komutuna yanıt verilmeyecektir. Ancak ağ iletişimi hedef cihazla hala devam etmelidir.

2) **Traceroute**

Traceroute, paketlerin hedeflerine ulaşana kadar izlediği rotayı belirlemek için kullanılan bir uygulamadır. Paketlerin takip ettiği yol haritasının tüm ayrıntıları bu uygulama aracılığıyla ortaya çıkar.

![traceroute-istegi](assets/icmp/traceroute-istegi.png)

Yukarıdaki resimde görüldüğü gibi "google.com"a ulaşılana kadar iletilen ağ cihazlarının IP adresleri "traceroute" komutuyla başarıyla görüntülenmiştir.

**NOT**: Windows işletim sisteminde Traceroute örnek kullanımı şöyledir:

**tracert google.com**