---
title: "Address Resolution Protocol (ARP)"
date: 2026-03-13 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, arp, address-resolution-protocol, adres-çözümleme-protokolü, arp-tablosu, arp-protokol-başlığı]
image:
    path: /assets/img/arp_Baslik.png
    alt: Address Resolution Protocol
---

## Adres Çözümleme Protokolü (ARP) Nedir?

Veri bağlantısı katmanı üzerinde çalışan ve cihazların iletişiminde önemli bir role sahip bir ağ protokolüdür. ARP protokolünün temel görevi, mantıksal ve fiziksel adreslerin birbirleriyle eşleştiğinden emin olmak ve bilinen bir IP adresine sahip bir cihazın MAC adresini tanımlamaktır.

## ARP Protokolünün Çalışma Yapısı

Bir ağdaki iki cihaz birbirleriyle iletişim kurmaya başladığında, hedef cihazın MAC adresi ve IP adresi bilinmelidir. ARP protokolü, bilinen bir IP adresine sahip bir cihazın MAC adresini belirlemeye yardımcı olur.

![arp-calisma](assets/arp/arp-calisma.png)

## ARP Tablosu

Ağdaki tüm cihazlar, ağdaki diğer cihazların IP adresi ve MAC adresi bilgilerini belirli bir süre için ARP tablolarında tutar. ARP tabloları sayesinde, hedef cihazın MAC adres bilgilerinin ağ paketini gönderecek cihazda olup olmadığı belirlenir. Ağdaki cihazlara doğrudan sorarak MAC adresine doğrudan ARP tablosuna kaydetmek "**dinamik**" bir süreçtir. Başka bir ARP tablosu kayıt işlemi türü de "**statik**" kayıt işlemidir. ARP tablosundaki gerekli değerler, statik bir kayıt türü eklemek için komut satırı aracılığıyla manuel olarak girilir. Aygıtta ARP tablosunu görüntülediğimizde kayıt türünü görebiliriz.

**ARP Tablosunu Windows'ta Görüntüleme**

"**arp -a**" komutu, Windows'ta ARP tablosunu görmek için kullanılır.

**ARP Tablosunu MacOS'ta Görüntüleme**

"**arp -a**" komutu, MacOS'ta ARP tablosunu görmek için kullanılır.

**ARP Tablosunu Linux'ta Görüntüleme**

Linux'ta ise ARP tablosunu görmek için "**sudo arp**" komutu kullanılır.

## ARP Protokol Başlığı

ARP protokolünün kendi başlık yapısı vardır. Protokolün başlığında birçok alan vardır. Protokolün bilgileri bu alanlara dahil edilmiştir.

![arp-baslik](assets/arp/arp-protokol-basligi.png)

**Hardware Type (Donanım Türü)**

Donanım türü alanındaki değer ağ türünü gösterir. Veri bağlantısı katmanındaki protokolü gösteren değeri içerir. "2 bayt" uzunluğundadır. Örneğin, bu alandaki "**0x0001**" değeri "**ethernet**" e sahip olduğumuzu gösterir.

**NOT**: "**0x**" ile başlayan değer "**onaltılık**" anlamına gelir.

**Protocol Type (Protokol Türü)**

Protokol türü alanındaki değer, protokolü ağ katmanında gösteren değeri gösterir. "2 bayt" uzunluğundadır. Örneğin, bu alandaki "**0x0800**" değeri bunun "**İnternet Protokolü (IP)**" olduğunu gösterir.

**Hardware Length (Donanım Uzunluğu)**

Donanım uzunluğu alanı, donanım adresinin uzunluğunu gösterir. "1 bayt" uzunluğundadır. Örneğin, MAC adresi ethernet için donanım adresi olarak kullanıldığından, MAC adresleri 6 bayt uzunluğunda olduğu için "6" değeri bu alana dahil edilmiştir.

**Protocol Lnegth (Protokol Uzunluğu)**

Protokol uzunluğu alanı protokol adresinin uzunluğunu gösterir. "1 bayt" uzunluğundadır. Örneğin, IPv4 adresi genellikle IP protokolü için kullanıldığından, IPv4 adresleri "4 bayt" uzunluğunda olduğu için "4" değeri bu alana dahil edilir.

**Operation Code (Operasyon Kodu)**

Operasyon kodu alanı, ARP protokolü çerçevesinin görevinin bulunduğu alandır. "2 bayt" uzunluğundadır. Örneğin, bu alanda "1" değeri varsa, bu bir "**ARP isteği**" türüdür ve bu alanda "2" varsa bu bir "**ARP yanıt**" türüdür.

**Sender Hardware Address (Gönderen Donanım Adresi)**

Gönderen donanım, çerçeveyi gönderen aygıtın donanım adresinin bulunduğu alandır. Örneğin, bu gönderenin MAC adresinin ethernet için olduğu alandır. Bu alanın uzunluğu protokole göre değişir. Ethernet protokolü kullanılıyorsa gönderen donanım adresinin uzunluğu 6 bayt olmalıdır.

**Sender Protocol Address (Gönderen Protokol Adresi)**

Gönderen protokol adresi alanı, gönderenin protokol adresinin bulunduğu yerdir. Örneğin, gönderenin IP adresinin IP protokolü için yazıldığı alandır. Bu alanın uzunluğu protokole göre değişir. IP protokolü kullanılıyorsa gönderen protokolü adresinin uzunluğu 4 bayt olmalıdır.

**Target Hardware Address (Hedef Donanım Adresi)**

Hedef donanım, çerçeveyi alacak cihazın donanım adresinin bulunduğu alandır. Örneğin, alıcının MAC adresinin ethernet için yazıldığı yerdir. Bu alanın uzunluğu protokole göre değişir.

**Target Protocol Address (Hedef Protokol Adresi)**

Hedef protokol adresi alanı çerçeveyi alacak cihazın protokol adresidir. Örneğin, IP protokolü için alıcının IP adresinin yazıldığı alandır. Bu alanın uzunluğu protokole göre değişir.