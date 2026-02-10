---
title: "Şüpheli Ağ Trafiği Analizi: Wireshark İncelemesi"
date: 2026-02-10 03:45:00 +0300
categories: [Playbooks, Network Forensics]
tags: [wireshark, pcap, blue-team, traffic-analysis]
---

## 1. Olayın Özeti (Executive Summary)

Bu çalışmada, şirket ağımızdaki bir sunucudan dışarıya (outbound) doğru gerçekleşen şüpheli veri transferini inceledik. **Wireshark** kullanılarak yakalanan paketler analiz edilmiş ve bir **Data Exfiltration** (Veri sızdırma) girişimi tespit edilmiştir.

> [!IMPORTANT]
> Analiz edilen PCAP dosyası yalıtılmış ortamda incelenmelidir.

---

## 2. Analiz Adımları

### Adım 1: Protokol Hiyerarşisi
İlk olarak `Statistics > Protocol Hierarchy` menüsünden ağ trafiğinin genel dağılımına baktık.

```bash
# Tshark ile hızlı analiz komutu:
tshark -r capture.pcap -q -z io,phs