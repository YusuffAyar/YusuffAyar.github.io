---
title: "OSI Referans Modeli Nedir?"
date: 2026-03-01 15:00:00 +0300
categories: [Bilgisayar Ağı, Network, İnternet, OSI Referans Modeli]
tags: [bilgisayar-ağı, network, internet, osi-referans-modeli, iso, physical, fiziksel, data-link, veri-bağlantısı, ağ, transport, taşıma, session, oturum, presentation, sunum, application, uygulama, katman]
image:
    path: /assets/img/osi_referans_modeli_girisBaslik.png
    alt: OSI Referans Modeli
---

## OSI REFERANS MODELİ NEDİR?

**Open System Interconnection (OSI)** referans modeli 1978 yılında **International Organization for Standardization (ISO)** tarafından geliştirilmiştir. OSI modeli, farklı işletim sistemleri arasında iletişimi sağlamak için oluşturulmuş bir modeldir. Bu modelle ağ yapılarını anlamak daha kolay hale geldi. Katmanlı bir mimariye sahiptir. OSI modelindeki her katmanın ayrı görevleri vardır. Bu katmanlar arasında hiyerarşik bir düzen vardır ve her katman bir sonraki katmana hizmet eder. OSI modelindeki katman sayısı 7'dir.

7) APPLICATION LAYER (UYGULAMA KATMANI)
6) PRESENTATION LAYER (SUNUM KATMANI)
5) SESSION LAYER (OTURUM KATMANI)
4) TRANSPORT LAYER (TAŞIMA KATMANI)
3) NETWORK LAYER (AĞ KATMANI)
2) DATA LINK LAYER (VERİ BAĞLANTISI KATMANI)
1) PHYSICAL LAYER (FİZİKSEL KATMAN)

Veri iletimi bu katmanlar aracılığıyla gerçekleştirilir ve kullanıcıya iletilir.

![osi-referans-modeli](assets/osi-referans-modeli-giris/osi_referans_modeli.png)

1) **Physical Layer (Fiziksel Katman)**

OSI modelindeki ilk katmandır. Bu katmanda, veriler iletişim kanalları boyunca bitler halinde iletilir. Fiziksel katman yalnızca veri iletiminden sorumlu olduğundan, ilettiği veri türü ve ne olduğu hakkında herhangi bir bilgiye sahip değildir. Bu katman için veriler sıralı bit dizilerinden oluşur.

2) **Data Link Layer (Veri Bağlantısı Katmanı)**

OSI modelindeki 2. katmandır. Bu katman, fiziksel katmandaki bitleri işler ve bir sonraki katmana gönderilmeye hazırlar. Bu katmandaki temel işlem fiziksel adreslemedir. OSI referans modelinde hata kontrolünden sorumlu ilk katman veri bağlantısı katmanıdır.

3) **Network Layer (Ağ Katmanı)**

OSI modelindeki 3.katmandır. Ağ katmanı, verileri hedef mantıksal adrese (IP Adresi) teslim etmekten sorumludur. Bu katmandaki temel işlem mantıksal adreslemedir.

4) **Transport Layer (Taşıma Katmanı)**

OSI modelinin 4.katmanıdır. Taşıma katmanı, iletim güvenliğinden sorumludur. Bu katman, verilerin hatasız iletimi için birçok ek kontrol sağlar ve bu kontroller sayesinde veri iletimi başarıyla gerçekleştirilir.

5) **Session Layer (Oturum Katmanı)**

OSI modelinin 5.katmanıdır. Oturum katmanı, sunum katmanının çalışması için gerekli hizmetleri sağlamaktan sorumludur. Bu katmandaki ana işlem oturum yönetimidir.

6) **Presentation Layer (Sunum Katmanı)** 

OSI modelindeki 6.katmandır. Sunum katmanı verilerin görüntülendiği katmandır. İki iletişim kuran düğüm, veri gösterimi için ortak bir dil kullanmalıdır. Bu katman sayesinde kullanılan dilde anlaşma yapılır.

7) **Application Layer (Uygulama Katmanı)** 

OSI modelindeki 7. ve son katmandır. Kullanıcıya en yakın katmandır ve kullanıcı düzeyinde OSI modelinde bulunan yapılara erişim sağlar.