---
title: "SIEM Nedir? Modern Siber Güvenliğin Merkezi Sinir Sistemi"
date: 2026-02-10 05:00:00 +0300
categories: [Siber Güvenlik, Blue Team]
tags: [siem, soc, log yönetimi, korelasyon, siber savunma]
image:
    path: /assets/img/siem.jpeg
    alt: SIEM
---

Günümüzün karmaşık siber tehdit ortamında, kurumların ağlarında gerçekleşen her aktiviteyi izlemesi ve anlamlandırması hayati bir zorunluluktur. İşte bu noktada **SIEM (Security Information and Event Management)** devreye girer. Bu makalede, SIEM teknolojisinin ne olduğunu, mimarisini ve siber savunma stratejilerindeki kritik rolünü inceleyeceğiz.

## SIEM Nedir?

**SIEM**, kurumun bilişim altyapısındaki çeşitli kaynaklardan (sunucular, güvenlik duvarları, ağ cihazları, uygulamalar vb.) log verilerini toplayan, bu verileri merkezi bir noktada birleştiren ve siber güvenlik tehditlerini tespit etmek için analiz eden bir teknoloji bütünüdür.

> SIEM, aslında iki farklı teknolojinin birleşimidir: **SIM (Security Information Management)** yani log toplama ve raporlama ile **SEM (Security Event Management)** yani gerçek zamanlı izleme ve olay analizi.
{: .prompt-info }

## Temel Çalışma Prensibi ve Bileşenler

Bir SIEM çözümünün başarısı, veriyi nasıl işlediğine bağlıdır. Modern bir SIEM mimarisi genellikle dört ana aşamadan oluşur:

### 1. Log Toplama (Log Collection)
Ağdaki tüm varlıklardan ham verilerin toplanmasıdır. Bu veriler `Syslog`, `WMI` veya `Agent` (ajan) bazlı yöntemlerle merkeze taşınır.

### 2. Normalleştirme (Normalization)
Farklı üreticilere ait cihazlar (örneğin Cisco firewall ve Windows sunucu) logları farklı formatlarda üretir. SIEM, bu farklı dilleri tek bir ortak dile çevirerek analizi mümkün kılar.

### 3. Korelasyon (Correlation)
SIEM'in beyni burasıdır. Normalleştirilmiş veriler arasındaki ilişkileri analiz eder.

> **Örnek Senaryo:** Bir kullanıcının VPN ile sisteme bağlandıktan 1 dakika sonra, veritabanından 500 MB veri çekmesi tek başına şüpheli olmayabilir. Ancak bu iki olay birleştirildiğinde bir "Veri Sızıntısı" şüphesi doğurur.
{: .prompt-tip }

### 4. Alarm ve Tepki (Alerting & Response)
Korelasyon kuralları bir tehdit tespit ettiğinde, güvenlik analistlerine (SOC ekibi) bir alarm üretilir veya SOAR entegrasyonu varsa otomatik bir aksiyon (örneğin IP engelleme) tetiklenir.

## SIEM İş Akışı Şeması

Aşağıdaki şema, ham log verisinin bir güvenlik olayına dönüşme sürecini özetlemektedir:



```text
+---------------------+       +------------------------+       +---------------------+
|   LOG KAYNAKLARI    | ----> | TOPLAYICI & NORMALİZE  | ----> |  KORELASYON MOTORU  |
+---------------------+       +------------------------+       +---------------------+
| - Firewall (Syslog) |       | - Format Çevirisi      |       | - Kural Eşleşmesi   |
| - Sunucular (WMI)   |       | - Veri Zenginleştirme  |       | - Davranış Analizi  |
| - Uygulamalar       |       | - Filtreleme           |       | - Tehdit İstihbaratı|
+---------------------+       +------------------------+       +----------+----------+
                                                                          |
                                                                          | (Tetikleme)
                                                                          v
                                                               +---------------------+
                                                               |    ALARM & TEPKİ    |
                                                               +---------------------+
                                                               | [!] SOC Uyarısı     |
                                                               | [!] Otomatik Blok   |
                                                               +---------------------+