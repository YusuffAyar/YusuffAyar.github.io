---
title: "Network Topologies"
date: 2026-02-27 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, topoloji, internet, ağ, fiziksel-topoloji, mantıksal-topoloji, halka, ring, yıldız, star, örgü, mesh, full-mesh, partial-mesh, ortak-yol, bus, noktadan-noktaya, point-to-point, ağaç, tree]
image:
    path: /assets/img/network_topologyBaslik.png
    alt: Ağ Topolojileri
---

## Ağ Topolojileri

Ağ topolojisi, bir bilgisayar ağının fiziksel veya mantıksal yapısını anlamak için görsel bir haritadır. Ağdaki cihazların veya kabloların konumları, ağ topolojisini belirleyen faktörler arasındadır. Bir ağ topolojisine sahip olmanın birçok faydası vardır. Örneğin, ağdaki bir cihaz görevini yerine getirmezse ağdaki diğer hangi cihaz veya cihazların etkileneceğini görmek mümkündür. Büyük bir ağın ağ topolojisine bakıyorsak, ağdaki alt ağları ve bağlı olduğu cihazları görmek mümkündür. Ağ topolojisi 2 türe ayrılır: 

### Physical Topology

**Fiziksel Topoloji**, ağdaki tüm cihazların ve bileşenlerin tam konumları açısından çizildiği bir topoloji türüdür. Bu topolojiye bakıldığında, hangi yollar ve cihazlar üzerinde hangi kablolamanın yapıldığı görülür. Çizimde görülenin fiziksel bir karşılığı vardır. Örneğin, A cihazından B cihazına giden yolda bir ağ aygıtı varsa, bu cihaz fiziksel topolojide görülür.

![Fiziksel-Topoloji](/assets/topoloji/fiziksel-topoloji.webp)

### Logical Topology

**Mantıksal Topoloji**, fiziksel topoloji gibi topolojideki cihazların tam konumunu göstermez. Genellikle fiziksel topolojiden daha az element içerir. Çünkü mantıksal topolojide veri akışı önemlidir. Örneğin, A cihazından B cihazına giden veriler, A cihazı ile B cihazı arasındaki C cihazının üzerinden geçerse topolojiye dahil edilmeyebilir ve C cihazının üzerinde görüntülenmesi gereken veriler üzerinde hiçbir etkisi yoktur. Bu topolojide, cihazların fiziksel yerleşiminden ziyade vurgulanması istenen şey veri akışının yoludur.

![Mantıksal-Topoloji](/assets/topoloji/mantiksal-topoloji.webp)

Bazı topolojiler aşağıda açıklanmıştır: 

### Ring Topology

**Halka Topolojisi**, kapalı döngü mantığında çalışır. Gönderilen veri, hedefe ulaşana kadar halkanın etrafında tek yönde hareket eder. Her düğüm, gelen verileri üzerinden geçirir ve hedefe ulaşmasını sağlar. Düğümler arasında hiyerarşik bir ilişki yoktur.

![Halka](/assets/topoloji/halka.png)

### Halka (Ring) Topolojisinin Avantajları ve Dezavantajları

**Avantajları**

* Yoğun veri trafiğinde veri yolu topolojisinden daha iyi performans gösterir.
* Merkezi bir düğüme ihtiyaç duymaz.
* Yeni bir düğüm eklemek için yalnızca 2 bağlantı değişikliği gerektirdiğinden kurulumu ve yapılandırılması kolaydır.
* Noktadan noktaya yapısı nedeni ile hata kontrolü ve onarımı kolayca yapılabilir.

**Dezavantajları**

* Veriyi iletmeyen bir ağ olduğunda, tüm ağ olumsuz etkilenir.
* Düğüm eklenirse veya taşınırsa tüm ağ olumsuz etkilenebilir.
* Ağdaki iletim gecikmesi, düğüm sayısıyla doğru orantılı olarak artar.
* Bant genişliği, cihazlar arasındaki tüm bağlantılarda paylaşılır.

### Star Topology

**Yıldız Topolojisindeki** her düğüm merkezi bir düğüme bağlıdır. Tüm veri akışı merkezi düğüm üzerinden yapılır. Yıldız topolojisi en yaygın bilgisayar ağı topolojilerindendir.

![star](assets/topoloji/star.jpg)

### Yıldız (Star) Topolojisinin Avantajları ve Dezavantajları

**Avantajları**

* Bir düğümün bağlantısı kesildiğinde diğer düğümler olumsuz etkilenmez.
* Düğümlerin eklenmesi veya kaldırılması durumunda, ağın çalışması kesintiye uğramaz.
* Yoğun trafik altında iyi performans sağlar.
* Birden fazla cihaza sahip büyük ağlarda kullanmak için uygundur.

**Dezavantajları**

* Her düğümün merkezi düğüme bağlanması için gereken kablolama nedeniyle maliyet yüksektir.
* Merkezi düğümün arızalanması durumunda, bağlı tüm düğümler olumsuz etkilenir. Bu nedenle bağlantılar bozulur.

### Mesh Topology

**Örgü Topolojisi**, merkezi düğümün olmadığı ve her düğümün doğrudan diğerine bağlanabileceği bir ağ topolojisidir. Örgü topolojisi büyük ağlar için uygun bir topoloji değildir. 2 türe ayrılır:

### Full-Mesh

**Tam Örgü Topolojisinde**, ağdaki her düğüm ayrı ayrı kablolama ile diğer tüm düğümlere bağlanır. Bu topolojide, iki düğüm arasındaki bağlantının kopması olası değildir. Çünkü bağlantı kurmanın alternatif yolları vardır.

### Partial-Mesh

**Kısmi Örgü Topolojisinde**, her düğüm diğer tüm düğümlere doğrudan bağlı olmasa da, büyük ölçüde birbirine bağlıdır. Tıpki tam örgü topolojisinde olduğu gibi, bağlantı kesilmesi durumunda hedef düğüme ulaşmanın alternatif yolları vardır.

![fullpartial](assets/topoloji/fullmesh&partialmesh.webp)

### Bus Topology

**Ortak Yol Topolojisi**, düğümlerin ortak bir yolda bulunduğu ve veri iletiminin bu yolda çift yönlü bir bağlantı ile yapıldığı bir topolojidir. Ortak yol topolojisinde, her düğüm kendisine ait olmasa bile iletilen her veriyi alır. Düğümler arasında hiyerarşik bir düzen olmadığından, iletim önceliği yoktur.

![bus](assets/topoloji/bus.png)

### Ortak Yol (Bus) Topolojisinin Avantajları ve Dezavantajları

**Avantajları** 

* Düğüm eklemek oldukça kolaydır.
* Küçük ağlar için kullanışlıdır.
* Ortak yolu uzatmak kolaydır.
* Tek bir kablo kullanımı maliyeti azaltır.

**Dezavantajları**

* Ağda yüksek bir paket kaybı olasılığı vardır.
* Bant genişliği ağdaki tüm düğümler arasında paylaşıldığı için performansı zarar görebilir.
* Ağdaki hatalardan etkilenme oranı yüksektir.
* İletimi sağlayan ana kabloda bir kırılma varsa, ağ ikiye bölünür ve paket iletiminde sorunlar ortaya çıkar.

### Point-To-Point Topology

**Noktadan Noktaya Topoloji**, en basit topolojidir ve birbirine bağlı iki düğümden oluşur. Örneğin, iki telefon arasında geçen bir arama noktadan noktaya topoloji oluşturur veya iki bilgisayar arasında doğrudan bir bağlantı varsa bu da bir noktadan noktaya topoloji oluşturur.

![pointtopoint](assets/topoloji/pointtopoint.jpg)

### Tree Topology

**Ağaç Topolojisi**, yıldız ve ortak yol topolojisini birbirine bağlayarak oluşan hibrit bir ağ topolojisidir. Ağaç topolojisinin hiyerarşik bir düzeni vardır ve her düğümün herhangi bir sayıda alt düğümü olabilir.

![tree](assets/topoloji/tree.jpg)