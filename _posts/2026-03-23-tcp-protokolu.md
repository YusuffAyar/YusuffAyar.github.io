---
title: "Transmission Control Protocol (TCP)"
date: 2026-03-23 15:00:00 +0300
categories: [Bilgisayar Ağı, Network]
tags: [bilgisayar-ağı, network, internet, tcp, transmission-control-protocol, iletim-kontrol-protokolü, tcp-protokol-başlığı]
image:
    path: /assets/img/tcp_Baslik.png
    alt: Transmission Control Protocol
---

## İletim Kontrol Protokolü (TCP) Nedir?

İletim Kontrol Protokolü (TCP), uygulamalar arasında güvenilir ve istikrarlı veri aktarımı sağlayan bir ağ protokolüdür. OSI modeline göre 4.katmanda bulunur.

## TCP Protokolünün Özellikleri

* İki uygulama arasındaki veri iletimini sağlar.
* Birden fazla bağlantıya izin verir.
* Bağlantı kurulmadan önce veri aktarımı yapılmaz.
* Gönderilen veriler için öncelik ve güvenlik tanımları yapılabilir. 
* Bir hata kontrolü yapar.
* Akış kontrolü sağlar.

## TCP Bağlantısının Kurulması (Three-way Handshake)

TCP protokolü üzerinden veri aktarmak için TCP bağlantısı kurulmalıdır. TCP bağlantısının kurulması, gönderenin ve alıcının her ikisinin de veri aktarımı için hazır olduğunu gösterir. 

Veri aktarımından önce kurulan TCP bağlantısına "**Üç Yönlü El Sıkışma (Three-way Handshake)**" denir. Üç yönlü el sıkışma aşağıdaki adımlardan oluşur:

* TCP bağlantısını kurmak isteyen gönderen taraf, "**SYN**" bayrağına ayarlanmış TCP segmentini alıcı tarafına gönderir.
* Bu segmenti aldıktan sonra, alıcı taraf gönderene "**SYN**" ve "**ACK**" bayraklarına ayarlanmış bir TCP segmenti iletir.
* Son aşama olarak, bu segmentin gönderen kısmı, "**ACK**" bayrağına ayarlanmış TCP segmentini alıcıya geri gönderir ve bağlantı kurulur.

![three-way-handshake](assets/tcp/three-way-handshake.png)

**NOT**: SYN ve ACK bayrakları, TCP protokol başlığı içindeki 1 bit alanlardır.

**Bayraklar**

1) **SYN (SYNCHRONIZE)**: Bir bağlantı başlatmak için kullanılır. Three-way Handshake'in ilk adımıdır.
2) **ACK (ACKNOWLEDGEMENT)**: Gönderilen verinin veya bağlantı isteğinin başarıyla alındığını onaylamak için kullanılır. TCP iletişiminin neredeyse her aşamasında aktiftir.

## TCP Veri Akışı ve İletim Güvenilirliği

TCP protokolünde gönderilen segmentler 8 bitlik veri biçimindedir. TCP protokolü, gönderilen ve alınan her biti işaretleyerek izler. İşaretleyerek gönderdiği her veri parçası için alıcıdan bir yanıt bekler. Alıcıdan gelen yanıttan sonra, bir sonraki veri parçası gönderilir ve aynı şekilde gönderilen bir sonraki veri parçası için alıcıdan bir yanıt beklenir. Bu işaretleme sistemi ile TCP protokolü iletim güvenirliğini sağlar ve verileri eksiksiz ve sıralı bir şekilde iletir.

TCP protokolü, bağlantı kurulması sırasında rastgele bir sayı belirler. Bu sayıya "**İlk Sıra Numarası (Initial Sequence Number)**" denir. Bu numara TCP bağlantısındaki ilk veri aktarımı için kullanılır. Ardından bu sayıya gönderilen bayt sayısı eklenerek yeni sayılar oluşturulur. Bu yeni ortaya çıkan sayıların her birine "**Sıra Numarası (Sequence Number)**" denir. TCP protokolü segmentin bu numaralara göre alıcı tarafından alınıp alınmadığını bilir.

TCP protokolü, güvenilir iletim sağlayan bir ağ protokolüdür. Önceki konuda açıklanan üç yönlü el sıkışma, TCP protokolünde iletim güvenilirliği sağlayan mekanizmalardan biridir. TCP protokolünün iletim güvenilirliğini sağlayan ana mekanizma, her bir TCP segmentinin gönderilip gönderilmediğini doğrulayan bir yapıya dayanmaktadır. Bu sistematik segment gönderimi sayesinde herhangi bir nedenle gönderilemeyen bir TCP segmenti varsa, o segment tekrar gönderilir ve alıcı tarafa teslim edilir.

## TCP Bağlantılarını Sonlandırma

TCP bağlantılarının sonlandırılması 4 adımda gerçekleşir:

1) TCP bağlantısını sonlandırmak isteyen taraf, hedef cihaza "**FIN**" bayrağı ayarlanmış TCP segmentini gönderir.
2) TCP segmentini aldıktan sonra, hedef cihaz "**FIN**" bayrağının ayarlandığını görür ve yanıt olarak "**ACK**" bayrağı ayarlanmış TCP segmentini gönderir.
3) Hedef cihaz, bağlantıyı sonlandırmak isteyen cihaza "**FIN**" bayrağı alınmış TCP segmentini gönderir.
4) Son adım olarak, bağlantıyı sonlandırmak isteyen cihaz, gelen TCP segmentine yanıt olarak "**ACK**" bayrağı alınmış TCP segmentini gönderir ve TCP bağlantısı sonlandırılır.

![fin-ack](assets/tcp/fin-ack.png)

**NOT**: **FIN** ve **ACK** bayrakları, TCP protokol başlığındaki 1 bitlik alanlardır. TCP bağlantıları "**RST**" bayrağıyla da sonlandırılabilir. **RST** bayrağı kullanılarak sonlandırılan TCP bağlantısı, anında ve tek taraflı bir bağlantı sonlandırmasıdır. Başka bir deyişle bağlantıyı sıfırlamak için "**RST**" bayrağı kullanılır.

**Bayraklar**

1) **FIN (FINISH)**: Bağlantıyı normal bir şekilde sonlandırmak için kullanılır. Gönderici taraf artık veri göndermeyeceğini bildirir.
2) **ACK (ACKNOWLEDGEMENT)**: Gönderilen verinin veya bağlantı isteğinin başarıyla alındığını onaylamak için kullanılır. TCP iletişiminin neredeyse her aşamasında aktiftir.
3) **RST (RESET)**: Bağlantıyı aniden kesmek veya geçersiz bir bağlantı isteğini reddetmek için kullanılır. Genellikle bir hata durumunda devreye girer.

## TCP Bağlantıları

TCP bağlantıları, cihazda TCP tabanlı iletimi ileten uygulamalar tarafından sıklıkla kullanılır. Uygulamaların TCP protokolüne bağlanabilmesi için protokolle ilgili bazı bilgiler kullanılır. Her TCP bağlantısı "**Kaynak IP Adresi - Kaynak Port Numarası**", "**Hedef IP Adresi - Hedef Port Numarası**" bilgilerinden oluşur.

## Port Nedir?

Portlar, uygulamaların birbirleriyle iletişim kurmak için kullandıkları iletişim noktalarıdır. Bir sunucuda aynı anda birçok hizmet bulunabilir. Port numaraları gelen talepleri netleştirir ve bize hangi hizmetlere ait olduklarını söyler. Bağlantı noktası esasen "**0-65535**" arasında bir değer alabilen bir sayıdır. Bazı port numaraları varsayılan olarak bazı protokoller tarafından kullanılır. Bağlantı noktası numaraları ve IP adresleri soket adresini oluşturur. Örneğin, "**192.168.5.102:8080**" (**IP Adresi:Port Numarası**) ifadesi "**:**" ile ayrılmış iki ayrı bilgi parçası içerir.

1) IP Adresi
2) Port Numarası

**Varsayılan TCP Portları**

Aşağıda en iyi bilinen protokoller için varsayılan bağlantı noktalarına örnekler verilmiştir:

* **FTP: 21**
* **SSH: 22**
* **Telnet: 23**
* **SMTP: 25**
* **DNS: 53**
* **HTTP: 80**
* **POP3: 110**
* **SMB: 445**

Varsayılan TCP portları ile ilgili daha fazla bilgiye aşağıdaki bağlantıdan ulaşabilirsiniz:

**https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers**

## TCP Protokol Başlığı

TCP protokolünün başlığında birçok protokole özgü veri alanı vardır. Bu veri alanları, TCP protokolünün gerektirdiği tüm bilgileri içerir. Aşağıdaki resim, TCP protokolünün başlığını ve alanlarını göstermektedir.

![tcp-protokol-başlığı](assets/tcp/tcp-protokol-baslik.png)

Her alan aşağıdaki başlıklarda kısaca açıklanmıştır:

**Source Port Number (Kaynak Port Numarası)**

Kaynak port numarası, gönderenin bağlantı noktası numarasının dahil edildiği alandır. "16 bit" uzunluğundadır.

**Destination Port Number (Hedef Port Numarası)**

Hedef port numarası, alıcının bağlantı noktası numarasının dahil edildiği alandır. "16 bit" uzunluğundadır.

**Sequence Number (Sıra Numarası)**

Sıra numarası alanı, TCP segmentlerinin iletimlerini izlemek için kullanılan numaradır. TCP segmentinde "**SYN**" bayrağı ayarlanmışsa, bu sayı "**İlk Sayı Numarası (Initial Sequence Number)**" değeridir. "32 bit" uzunluğundadır.

**Acknowledgement Number (Onay Numarası)**

Onay numarası alanı, gönderilen segmentlerin iletiminin hangi bayta kadar yapıldığını gösteren bir değerdir. "32 bit" uzunluğundadır.

**Header Length (Başlık Uzunluğu)**

Başlık uzunluğu, TCP başlık uzunluğunun değerini tutan alandır. "4 bit" uzunluğundadır.

**Reserved (Ayrılmış)**

İleride kullanılmak üzere ayrılmış alandır. "3 bit" uzunluğundadır.

**Control Flags (Kontrol Bayrakları)**

Kontrol bayrakları, bayrakların değerlerinin tutulduğu alandır. Her bayrak "1 bit" uzunluğundadır. Bir bayrak ayarlamak, ikili olarak "1" değerini aldığı anlamına gelir. Toplamda, bu alan "9 bit" uzunluğundadır.

* **SYN**: TCP bağlantılarını başlatmak için kullanılan bayraktır.
* **ACK**: Bayrakların iletildiğini gösteren onay bayrağıdır. Ayrıca bağlantı kurulumunu onaylamayı da belirtir.
* **FIN**: TCP bağlantısını kontrollü bir şekilde sonlandırmak için kullanılan bayraktır.
* **RST**: TCP bağlantısını tek taraflı ve aniden sonlandırmak için kullanılan bayraktır. Bağlantıyı sıfırlamak için kullanılır.
* **PSH (PUSH)**: Verilerin hedef uygulamaya gönderildiği paketlerde ayarlanan bayraktır.
* **URG (URGENT)**: Acil ve öncelikli veriler olduğunu belirtmek için kullanılan bayraktır.

**Windows Size (Pencere Boyutu)**

Pencere boyutu alanı, alıcının arabellek kapasitesinin maksimum veri boyutunun tanımlandığı yerdir. "16 bit" uzunluğundadır.

**Checksum (Sağlama Toplamı)**

Sağlama toplamı, iletim sırasında TCP segmentinin bütünlüğünün sağlam olup olmadığını kontrol eden alandır. Onaltılık değere sahiptir ve "16 bit" uzunluğundadır.

**Urgent Pointer (Acil İşaretçi)**

Acil işaretçi alanı, acil baytların hangi verilere kadar olduğunu gösteren bir değerdir. Bu alanı kullanmak için "**URG**" bayrağı ayarlanmalıdır. "16 bit" uzunluğundadır.

**Options (Seçenekler)**

Seçenekler, çeşitli TCP protokolü ek özelliklerini kullanmak için oluşturulan alandır. Kullanma zorunluluğu yoktur. Sabit bir uzunluğu yoktur.