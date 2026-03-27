---
title: "User Datagram Protocol (UDP)"
date: 2026-03-23 18:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, udp, user-datagram-protocol, kullanıcı-datagram-protokolü, udp-protokol-başlığı]
image:
    path: /assets/img/udp_Baslik.png
    alt: User Datagram Protocol
---

## Kullanıcı Datagram Protokolü (UDP) Nedir?

Kullanıcı Datagram Protokolü (UDP), uygulamalar arasında veri iletimi sağlayan başka bir ağ protokolüdür. OSI modelinin 4. katmanında bulunur. TCP protokolünün aksine, UDP protokolü iletim güvenilirliği sağlamaz.

## UDP Protokolünün Özellikleri

* İletimden önce bağlantı kurulumu gerektirmez.
* Hızlı bir iletim sağlar.
* Verilerin iletileceğini garanti etmez.
* Başlık yapısında daha az bilgi içerir.
* Genellikle video uygulamaları ve gerçek zamanlı uygulamalar tarafından kullanılır.
* Hata kontrolü yapmaz.
* Akış kontrolünü işlemez.

## UDP Bağlantıları

UDP bağlantıları, UDP üzerinden veri ileten uygulamalar tarafından sıklıkla kullanılır. Uygulamaların UDP protokolüne bağlanması için protokolle ilgili bazı bilgiler kullanılır. Her UDP bağlantısı "**Kaynak IP Adresi - Kaynak Port Numarası**", "**Hedef IP Adresi - Hedef Port Numarası**" bilgilerinden oluşur.

**Varsayılan UDP Portları**

Aşağıda en iyi bilinen protokoller için varsayılan port numaralarına örnekler verilmiştir:

* **DNS: 53**
* **DHCP: 67, 68**
* **SNMP: 161, 162**

Varsayılan UDP portlarının daha büyük bir listesini şu adreste bulabilirsiniz:

**https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers**

## UDP Protokol Başlığı

UDP protokol başlığındaki alanlar diğer ağ protokollerinden çok daha azdır. Aşağıdaki resim UDP protokolünün başlıklarını ve alanlarını göstermektedir:

![udp-protokol-baslik](assets/udp/udp-protokol-baslik.png)

**Source Port Number (Kaynak Port Numarası)**

Gönderenin port numarasını içeren alandır. "16 bit" uzunluğundadır.

**Destination Port Number (Hedef Port Numarası)**

Alıcının port numarasını içeren alandır. "16 bit" uzunluğundadır.

**Length (Uzunluk)**

UDP segmentinin başlığının ve verilerinin toplam uzunluğunu içeren alandır. "16 bit" uzunluğundadır.

**Checksum (Sağlama Toplamı)**

Sağlama toplama alanı, iletim sırasında UDP segmentinin bütünlüğünün sağlam olup olmadığını kontrol etmeye izin veren onaltılık değeri içerir. TCP protokolünün aksine, bu alan gerekli değildir. "16 bit" uzunluğundadır.