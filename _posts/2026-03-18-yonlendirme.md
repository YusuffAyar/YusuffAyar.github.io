---
title: "Routing"
date: 2026-03-18 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, routing, yönlendirme, static-routing, dynamic-routing, default-routing, statik-yönlendirme, dinamik-yönlendirme, varsayılan-yönlendirme, yönlendirme-tablosu, ip-yönlendirme-algoritması, yönlendirme-protokolleri, rip, ospf, igrp, eigrp]
image:
    path: /assets/img/routing_Baslik.png
    alt: Routing
---

## Yönlendirme (Routing) Nedir?

Bir ağdan farklı ağlara iletim ve iletim yolunun belirlenmesine "**yönlendirme (routing)**" denir. Yönlendiriciler, yönlendirmenin ana görevi olan cihazlardır. Yönlendirici cihazlarında en az 2 ağ arayüzü vardır.

## Yönlendirme Tablosu

Yönlendirme tablosu, ağın cihazlara gidebileceği rotaların bilgilerinin bulunduğu yerdir. Cihazlar bu tabloları yönlendirmede kullanır.

![routing](assets/routing/routing.png)

Yukarıdaki resimde gösterildiği gibi, yönlendirme tablosu "netstat -nr -f inet" komutuyla başarıyla görüntülenmiştir.

* **-n**: Adresleri isim olarak çözmek yerine IP olarak gösterir. Bu, çıktının daha hızlı gelmesini sağlar.
* **-r**: Yönlendirme tablolarını gösterir.
* **-f inet**: Sadece IPv4 kayıtlarını filtreler.

**NOT**: Windows işletim sisteminde yönlendirme tablosunu görüntülemek için aşağıdaki örnek komutu kullanabiliriz:

**route PRINT -4**

## Yönlendirme Türleri

3 farklı yönlendirme türü vardır.

![yonlendirme-tablolari](assets/routing/routing-turleri.png)

1. **Static Routing (Statik Yönlendirme)**

Ağ yöneticilerinin yönlendirme tablolarına sabit bir rotanın eklenmesine izin veren manuel yönlendirme girişleridir. Bu kayıt zamanla asla değişmeyecektir. Değişiklik yalnızca ağ yöneticisi yönlendirme tablolarında değişiklik yaparsa gerçekleşebilir.

2. **Dynamic Routing (Dinamik Yönlendirme)**

Statik yönlendirmenin aksine, dinamik yönlendirme zamana ve duruma bağlı olarak değişebilen yönlendirme türüdür. Dinamik yönlendirmeyi yönetmekten sorumlu yönlendirme protokolleri vardır.

3. **Default Routing (Varsayılan Yönlendirme)**

Diğer rotaların kendileri için uygun olmadığını belirleyen cihazlar varsayılan yönlendirmeyi kullanır. Ayrıca, iletişimde yalnızca bir yön olduğunda varsayılan yönlendirme, yönlendirme tablosuna eklenir.

## IP Yönlendirme Algoritması

Paketlerin iletilebilmesi için iletişimdeki cihazların belirli kararlar alması gerekir. Hangi paketin hangi hedefe gideceği cihaz tarafından bilinmelidir. Bunu sağlayan en önemli mekanizmalardan biri IP yönlendirme algoritmasıdır. IP yönlendirme algoirtması temel olarak aşağıdaki gibi çalışır.

1. Hedef IP adresi bilgileri gelen IP paketi aracılığıyla elde edilir.
2. Elde edilen IP adresi bilgilerinin hangi ağa ait olduğu ağ adresi hesaplanarak belirlenir.
3. Ağ adresi gerçekten de cihazda bulunan ağsa, hedefin MAC adresi olduğu ve iletişimin gerçekleştirildiği anlamına gelir.
4. Ağ adresi cihazda bulunan ve ağdan başka bir adres gösteriyorsa, yönlendirme tablosu analiz edilerek paketin hangi cihaza gönderileceği belirlenir.
5. Yönlendirme tablosunda uygun bir rota yoksa paket varsayılan ağ geçidine gönderilir.
6. Varsayılan ağ geçidine paket iletimi gerçekleşmezse, ICMP hata mesajı üretilir.

## Yönlendirme Protokolleri

Birçok farklı algoritmaya sahip yönlendirme protokolleri vardır. Gerekirse yönlendiricilerde farklı yönlendirme protokolleri kullanılabilir. Bazı yönlendirme protokolleri şunlardır:

* **RIP (Routing Information Protocol)**
* **OSPF (Open Shortest Path First)**
* **IGRF (Interior Gateway Routing Protocol)**
* **EIGRP (Enhanced Interior Gateway Routing Protocol)**