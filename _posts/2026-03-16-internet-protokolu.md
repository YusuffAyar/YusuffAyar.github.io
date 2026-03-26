---
title: "Internet Protocol (IP)"
date: 2026-03-16 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, ip, internet-protokolü, internet-protocol, internet-protokol-başlığı]
image:
    path: /assets/img/ip_protokol_Baslik.png
    alt: Internet Protocol
---

## İnternet Protokolü (IP) Nedir?

İnternet protokolü, farklı ağlar arasında paket iletimini sağlayan protokoldür. Verileri bir üst iletim katmanına gönderilecek şekilde hazırlar.

## IP Protokolünün Özellikleri

1. Veri iletimi altında gönderilecek büyük paketleri daha küçük parçalara bölme işlemini gerçekleştirir.
2. Güvenilir iletim için akış kontrol mekanizması gerekmez.
3. OSI katmanlarındaki en işlevsel yapıdır.
4. Üst katmana ilettiği paketler kolayca taklit edilebildiğinden, kontrol ve güvenlik mekanizmaları üst katmanlara aittir.
5. İnternet Protokolü (IP) mantıksal adresler kullanarak çalışır.

## IP Protokol Başlığı

IP protokolü başlıkları bir çok alan içerir.

![ip-protokol-basligi](assets/ip-protokolu/ip-protokol-basligi.png)

**Version (Sürüm)**

Sürüm alanı, IP paketinin türünün tanımlandığı yerdir. Bu alandaki değere göre IP paketinin IPv4 veya IPv6 olup olmadığını gösterir. "4 bit" uzunluğundadır.

**Internet Header Length (İnternet Başlık Uzunluğu)**

Değişken alabilen IP başlığının uzunluğunun gösterildiği alandır. En küçük IP paket başlığı 20 bayttır. "4 bit" uzunluğundadır.

**Types of Service (Hizmet Türleri)**

Hizmet kalitesi (QoS) parametrelerinin bulunduğu alandır. "8 bit" uzunluğundadır.

**Total Length (Toplam Uzunluk)**

Toplam uzunluk alanı, IP başlığını ve verilerin toplam uzunluğunu ifade eder. "16 bit" uzunluğundadır.

**Identification (Tanımlama)**

Tanımlama alanı, her bir IP paketinin kimlik numarasını gösteriri. "16 bit" uzunluğundadır.

**IP Flags (IP Bayrakları)**

IP bayrakları, pakette IP parçalanmasının uygulanıp uygulanmadığını gösteren alandır. "3 bit" uzunluğundadır.

**Fragmentation Offset (Parçalanma Ofseti)**

Parçalanma ofseti alanı, parçalanmış paketin kaç bayt olduğunu gösterir. "13 bit" uzunluğundadır.

**Time to Live (Yaşama Zamanı)**

Yaşama zamanı (TTL), paketin alabileceği atlama sayısını gösterir. Paketin bir cihazdan diğerine iletilmesi "1 atlama" anlamına gelir ve her atlamada TTL'deki değer "1" azalır. "0" değerine ulaşan paket artık iletilmez. TTL Alanı "8 bit" uzunluğundadır.

**Protocol (Protokol)**

Protokol alanındaki değer, paketin bir üst katmanda ilişkilendirildiği protokolü gösterir. "8 bit" uzunluğundadır.

**Header Checksum (Başlık Kontrol Toplamı)**

IP başlığının sağlam bir şekilde iletilip gönderilmediğini görmek için hesaplayan kontrol değeridir. Belirli bir algoritma tarafında hesaplanan bu değer doğrulama amacıyla kullanılır. "16 bit" uzunluğundadır.

**Source Address (Kaynak Adresi)**

Kaynak adresi alanı, paketi gönderen IP adresidir. "32 bit" uzunluğundadır.

**Destination Address (Hedef Adresi)**

Hedef adresi alanı, alıcının IP adresinin bulunduğu yerdir. "32 bit" uzunluğundadır.

**Data (Veri)**

Veri alanı, alt katmandaki toplam verilerin bulunduğu alandır.