---
title: "Data Encapsulation and Decapsulation in the OSI Model"
date: 2026-03-11 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, protokol, protocol, communication, iletişim, management, yönetim, security, güvenlik, arp, ip, tcp, udp, bgp, dhcp, icmp, snmp, ftp, pop3, telnet, ssl, tls]
image:
    path: /assets/img/ag_protokolleriBaslik.png
    alt: Network Protocols
---

## OSI Modelinde Veri Akışı

OSI Modeli hiyerarşik ve katmanlı bir mimariye sahiptir. Veri akışı, OSI modelindeki katmanlar arasında belirli bir yönde hareket eder.

![veri-akışı](assets/osi-kapsulleme/osi-veri-akisi.png)

## OSI Modelinde Veri Kapsülleme ve Dekapsülasyon İşlemi

Katmanların bazı başlık bilgileri, alıcı tarafında ihtiyaç duyulduğu gibi OSI modelindeki veri akışı sırasında ham verilere eklenir. Uygulamada çıkan ham verilerin yanına her katman için başlık bilgisi ekleme işlemene "**Kapsülleme(Encapsulation)**" denir. Gönderen tarafında gerçekleşen bu sürecin tersi alıcı tarafında da gerçekleştirilir. Her katman için başlık bilgileri, uygulama katmanından fiziksel katmana kadar olan toplam verilere dahil edilebilir. Bu nedenle alıcı tarafında ters yönde (fiziksel katmandan uygulama katmanına), her katman kendi başlık bilgilerini alır ve sorumlu olduğu üst katmana iletir. Bu şekilde uygulama içinde ham veriler elde edilir ve işlenir. Bu işleme alıcı tarafında "**Dekapsülasyon(Decapsulation)**" denir.


