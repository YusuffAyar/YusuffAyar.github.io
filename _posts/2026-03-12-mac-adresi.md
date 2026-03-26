---
title: "Media Access Control (MAC) Address"
date: 2026-03-12 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, mac-adresi, media-access-control, address, adres, interface-card, ağ-arayüz-kartı]
image:
    path: /assets/img/mac_adresiBaslik.png
    alt: MAC Adresi
---

## Ağ Arayüz Kartı (Network Interface Card) Nedir?

Bilgisayarlarda ağ bağlantılarını ve iletişimlerinin kurulmasını ve sürdürülmesini sağlayan bir donanımdır. Ağ iletişimlerinde gelen ve giden ağ paketleri, ağ arayüz kartları sayesinde alınır/iletilir. Çeşitli boyutlarda ve özelliklerde birçok **NIC** donanım türü vardır. Örneğin, kablosuz iletişim sağlayan NIC'ler vardır. **Wi-Fi** "**kablosuz NIC**" donanımının kullanıma sunduğu bir özelliktir. Ağ arayüz kartları olmadan ağ iletişimi mümkün olmazdı.

![interface-card](assets/mac-adresi/network-interface-card.jpg)

## MAC (Media Access Control) Adresi Nedir?

**Medya Erişim Kontrolü (MAC)** adresi, ağ iletişimi için gerekli olan fiziksel adrestir. IP adresi ve MAC adresi, bir cihazda hiçbiri olmadan kurulamayan ağ iletişimini sağlamak için birlikte yer alır. MAC adresleri üretim sırasında NIC'lere yerleştirilir. Üretilen NIC donanımlarının her birinin benzersiz bir MAC adresi vardır. MAC adresi "6 bayt" (48 bit) uzunluğundadır. On altılık olarak ifade edilir.

**Örnek MAC Adresi: 2C:54:91:88:C9:E3**

MAC adresinin ilk 3 baytı, satıcılara özgü ilgili kuruluşlardan elde edilir. Son 3 baytı satıcı tarafından belirlenir. Bu şekilde, her MAC adresi benzersiz bir adres haline gelir.

## MAC Adresi Satıcı Bulma

Çevrimiçi hizmetleri kullanarak MAC adresinin ait olduğu satıcıyı belirleyebilirsiniz.

**Bazı MAC Adresi Satıcıları:** 

**https://macvendors.com**

![mac-vendors](assets/mac-adresi/mac-vendors.png)

**https://macaddress.io**

![mac-address-io](assets/mac-adresi/mac-address-io.png)

Girilen MAC adresinin detaylı bilgilerini Search tuşuna bastıktan sonra aşağıdaki gibi görebiliriz.

![mac-address-io](assets/mac-adresi/mac-address-io-sonuc.png)

Bu çevrimiçi hizmetleri kullanmadan satıcının bilgilerini bulmak da mümkündür. Bunun için listeler vardır. Örneğin, MAC adresinin ilk 3 baytını sorgulayabilir ve satıcı bilgilerini alabiliriz.

**MAC Satıcıları Listesi: https://gist.github.com/aallan/b4bb86db86079509e6159810ae9bd3e4**

Bazı MAC adreslerinin satıcı bilgileri çevrimiçi hizmetler veya listeler aracılığıyla bulunmayabilir. Bu nedenle, aradığımız MAC adresinin satıcı bilgilerini bulma olasılığını artıracak tek bir kaynak yerine birden fazla kaynağı kontrol etmek her zaman iyidir.

**Windows'ta Ağ Arayüzlerinin MAC Adreslerini Görüntüleme**

Windows'ta MAC adreslerini görüntüleyebilmek için komut satırı üzerinden "**ifconfig /all**" komutunu kullanabiliriz.

**MacOS İşletim Sistemi Ağ Arayüzünde MAC Adresini Görüntüleme**

MacOS'te MAC adreslerini görüntüleyebilmek için komut satırı üzerinden "**ifconfig**" komutunu kullanabiliriz.



**Linux'ta Ağ Arayüzlerinin MAC Adreslerini Görüntüleme**

Linux'ta MAC adreslerini görüntüleyebilmek için komut satırı üzerinden "**ifconfig**" komutunu kullanabiliriz.