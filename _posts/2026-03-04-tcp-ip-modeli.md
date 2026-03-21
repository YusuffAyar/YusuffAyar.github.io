---
title: "TCP/IP Model"
date: 2026-03-04 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, osi-referans-modeli, tcp-ip-modeli, network-access, ağ-erişimi, ağ, transport, taşıma, application, uygulama, layer, katman]
image:
    path: /assets/img/tcp_ipBaslik.jpg
    alt: TCP/IP Modeli
---

## TCP/IP Modeli

1960'larda ABD Savunma Bakanlığı (DoD) tarafından tasarlanmış ve geliştirilmiştir. TCP/IP modeli tanıtıldığında, henüz bilgisayar ağ iletişiminde standartları belirleyen bir model yoktu. Bu modelle internet temelinde ağ iletişiminin nasıl olması gerektiği belirlendi. TCP/IP modeli katmanlı bir mimariye sahiptir ve 4 katmandan oluşur.

4. APPLICATION LAYER (UYGULAMA KATMANI)
3. TRANSPORT LAYER (TAŞIMA KATMANI)
2. NETWORK LAYER (AĞ KATMANI)
1. NETWORK ACCESS LAYER (AĞ ERİŞİMİ KATMANI)

![tcp-ip](assets/tcp-ip-modeli/tcp-ip.jpeg)

1) **Network Access Layer (Ağ Erişimi Katmanı)**

TCP/IP modelindeki 1.katmandır. OSI referans modelindeki 1. ve 2. katmanlara karşılık gelir. Bu katman fiziksel erişimleri ve donanım kontrollerini içerir.

2) **Network Layer (Ağ Katmanı)**

TCP/IP modelindeki 2.katmandır. OSI referans modelinde katman 3 ile benzer işlevlere sahiptir. Bu katmanda, ağ iletişim işlevleri mantıksal adresleme ile gerçekleştirilir.

3) **Transport Layer (Taşıma Katmanı)**

TCP/IP modelindeki 3.katmandır. OSI referans modelinde katman 4 ile benzer işlevlere sahiptir. Bu katmanda veri iletimi yapılır ve iletişimin güvenilirliği sağlanır. Verilerin bozulma olmadan doğru şekilde iletilip iletilmediği bu katmanda yönetilir.

4) **Application Layer (Uygulama Katmanı)**

TCP/IP modelindeki 4. ve son katmandır. OSI referans modelinde 5., 6. ve 7. katmanlarda gerçekleştirilen tüm işlemleri kapsayan bir katmandır. Uygulama düzeyinde kontroller ve işlemler bu katmanda yürütülür.

## OSI Modeli ve TCP/IP Modeli

OSI referans modeli ve TCP/IP modeli çok benzer modeller olmasına rağmen, bazı noktalarda birbirlerinden farklıdırlar. TCP/IP modeli ilk ortaya çıktığında, standart olmayı hedeflemeden zorunluluktan ortaya çıktı. Öte yandan OSI referans modeli, pratik kullanımı da dahil olmak üzere teoride olması gereken ideal ağ iletişimini tasarlamayı amaçlamıştır. TCP/IP modeli bazı protokollere dayanarak geliştirilmiştir. Öte yandan OSI modeli herhangi bir protokolde geliştirilmemiştir.

![osi-tcp-ip](assets/tcp-ip-modeli/osi-tcp-ip-modeli.png)