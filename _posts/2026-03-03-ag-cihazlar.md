---
title: "Network Devices"
date: 2026-03-03 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, ağ-cihazları, switch, router, hub, repearter, bridge, modem, firewall, gateway, anahtar, yönlendirici, tekrarlayıcı, köprü, güvenlik-duvarı, ağ-geçidi]
image:
    path: /assets/img/ag_cihazlariBaslik.png
    alt: Ağ Cihazları
---

## Ağ Cihazları

Bir bilgisayar ağında, her biri ayrı bir görevden sorumlu ağ cihazları vardır. Bir bilgisayar ağında bu bileşenler olmadan, ağ görevleri yerine getiremez. Bu nedenle, ağ cihazlarının görevlerini ve yeteneklerini bilmek, ağdaki sorunları çözmeye ve güvenlik ihlallerini anlamaya olanak tanır. Bu şekilde hızlı bir şekilde harekete geçilerek çözüme ulaşılır.

1) **Switch**

OSI referans modeline göre katman 2'de çalışan ağ cihazlarından birisidir. Bununla birlikte, daha yönetilebilir özelliklere sahip bazı switchler, OSI referans modeline göre katman 3'te çalışır. Switchler ara bağlantı cihazlarıdır. Ağa bağlanmak isteyen düğümleri bağlamak için kullanılır. Boyutlar, üzerindeki bağlantı noktası sayısına bağlı olarak değişebilir.

Switch cihazı kaynak bağlantı noktasından gelen verileri yalnızca hedef bağlantı noktasına iletir, bu nedenle ağ performansını olumsuz etkilemeyecek bir veri iletimi sağlar. Güvenlik açısından, iki tarafa ait verilerin üçüncü taraflara ulaşmasını önler ve böylece veri güvenliğini bir şekilde artırmış olur.

![switch](assets/ag-cihazlari/switch.jpeg)

2) **Router**

OSI referans modeline göre 3.katmanda çalışan ağ cihazlarından birisidir. Router, bir işletim sistemi (**IOS-Internet Operating System**) içeren son derece gelişmiş özelliklere sahip bir paket yönlendirme cihazıdır. İki bilgisayar ağı arasına yerleştirilerek kurulan ağ cihazıdır. Genellikle **LAN-LAN** bağlantılarında ve **WAN-LAN** bağlantılarında kullanılır. Router'ın en temel görevi paket yönlendirmesidir. Router sayesinde ağlar birbirinden ayrılır. Bilgisayar ağlarını birbirinden ayıran cihazdır. Yapılandırılabilir bir cihazdır.

![router](assets/ag-cihazlari/router.jpg)

3) **Hub**

OSI referans modeline göre katman 1'de çalışan ağ cihazıdır. Çok basit bir yapıya sahip olan hub cihazı, ağa bağlanmak isteyen bilgisayarları bağlamak için kullanılan cihazlardan biridir.

![hub](assets/ag-cihazlari/hub.jpg)

4) **Repeater**

OSI referans modeline göre katman 1'de çalışan ağ cihazlarından biridir. Repeater cihazında 2 bağlantı noktası vardır. Bu portlar gelen sinyali giden bir sinyale dönüştürür ve hedefe iletir. Üzerindeki zayıf sinyalleri güçlendirir. Verileri daha uzun mesafelere iletmesini sağlar. Hub'a benzer bir cihazdır ancak bir hub kadar çok bağlantı noktasına sahip değildir.

![repeater](assets/ag-cihazlari/repeater.jpg)

5) **Bridge**

OSI referans modeline göre katman 2'de çalışan ağ donanımlarından biridir. Bridge, iki bilgisayar ağını bağlayarak paket yönlendirmesi gerçekleştirir. Bir Router'a benzer bir göreve sahip olmasına rağmen, bir Router'dan daha az bağlantı noktasına sahip çok basit bir cihazdır. Ayrıca 2.katmanda çalışarak Router'dan ayrılır. Bridge **LAN-LAN** bağlantılarında kullanılır.

![bridge](assets/ag-cihazlari/bridge.jpg)

6) **Modem**

Modemler genellikle switchler gibi bazı cihazların özelliklerinin bir araya getirildiği küçük boyutlu ağ cihazıdır. Küçük bir işletim sistemi içerir. Genellikle ev ağlarında internete erişmek için kullanılır. Üzerinde bir veya birden fazla bağlantı noktası olabilir. Ayrıca, kablosuz destekli modemlerde modemle birlikte kablosuz cihazlar kullanarak internet bağlantısı sağlamak mümkündür.

![modem](assets/ag-cihazlari/modem.png)

7) **Firewall**

OSI referans modeline göre katman 4'te çalışan ağ cihazıdır. Firewall, güvenli olmayan bir ağ olarak kabul edilen internet ile mevcut ağ arasında bulunan ağ donanımı için hayati öneme sahiptir. Ağın güvenliğini sağlamak için gerekli olan temel ağ cihazlarından biri olan Firewall'un görevi, trafiği belirli kurallara göre engellemek veya izin vermektir. Birçok türü olmasına rağmen, en yaygın kullanılan ve bilinen güvenlik duvarı türü donanım ağı güvenlik duvarı cihazlarıdır. Tek başına bir Firewall cihazına sahip olmak, ağı dış tehditlere karşı korumak için yeterli değildir. Çünkü saldırganlar güvenlik duvarıları ile ağlara bile sızabilirler. Firewall doğru şekilde yapılandırılmalıdır. Eksik ve yanlış Firewall yapılandırmaları, ağ performansını olumsuz etkileyebilir ve güvenlik açıklarına neden olabilir.

![firewall](assets/ag-cihazlari/firewall.png)

8) **Gateway**

OSI modeline göre her katmanda çalışabilen ağ cihazlarından birisidir. Gateway, iki ağ arasında bulunan ağlar arası iletişim sağlayan bir ağ bileşenidir. Ağları birbirine bağlar. Görevi açısından Router cihazlarına benzer olmasına rağmen, her katmanda çalışma yeteneği ile Router'dan farklıdır. Ek olarak, sadece donanım değil aynı zamanda yazılım ağ geçidi türleri de vardır. Gateway, ağdaki diğer düğümler için bir ağ geçididir. Bu cihaz aracılığıyla ağdan çıkıp başka bir ağdaki bir düğümle iletişim kurabilirler.

![gateway](assets/ag-cihazlari/gateway.jpg)