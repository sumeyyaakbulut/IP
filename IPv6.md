# IPv6
IPv6(İnternet Protokolü) Sürüm 6, iletişimin ağ üzerinden gerçekleşmesine izin veren bir ağ katmanı protokolüdür. IPv4, internet protokolü dünyasında bir dönüm noktası olmuş ve milyarlarca cihazın birbirine bağlanmasını mümkün kılan 32 bitlik bir adresleme sistemini tanıtmıştır. Ancak, IPv4'ün kullanılabilir adres sayısı sınırlıdır ve bu durum, internetin hızla büyümesiyle birlikte ciddi bir sorun haline gelmiştir. IPv4, toplamda 4.294.967.295 adet (yaklaşık 4.3 milyar) IP adresi sağlayabilir. 

IPv4, A, B ve C sınıfı adres aralıkları ile farklı büyüklükteki ağlara IP adresi ataması yapılıyordu. Örneğin, C sınıfı 256 IP adresi, B sınıfı 65.535 IP adresi ve A sınıfı 16.777.216 IP adresi sağlardı. Büyük şirketler, özellikle A sınıfı ağları kullanarak milyonlarca IP adresine sahip oldular. Ancak, bu büyük blokların birçoğu tam anlamıyla kullanılmadı ve birçok IP adresi boşa harcandı.

IPv4, değişken Uzunluklu Alt Ağ Maskesi (VLSM) ve Network Address Translation (NAT) gibi teknolojiler, IP adreslerini daha etkili bir şekilde kullanmamıza yardımcı oldu. VLSM, istediğimiz alt ağ maskesini kullanarak daha küçük alt ağlar oluşturmamıza izin verdi. NAT ve Port Address Translation (PAT) ise bir genel IP adresinin arkasında birçok özel IP adresini paylaşmamıza olanak tanıdı.

Ancak, internetin hızlı büyümesi ve cihaz sayısındaki patlama, bu önlemlerin sınırlarını zorladı. VLSM ve NAT/PAT gibi çözümlere rağmen, IPv6'nın getirdiği 128 bitlik adresleme sistemi (2^128 sayısı yani 340 undecilyon civarında IP adresi sağlayabilir), çok daha geniş bir adresleme alanı sağlayarak gelecekteki büyüme ve genişleme ihtiyaçlarına cevap vermeyi hedefler. IPv6, internetin daha sürdürülebilir ve genişletilebilir olmasını sağlamak için önemli bir adımdır.

IPv6 sadece daha uzun adreslerden ibaret değil. IPv6'nin hedefleri, uçtan uca güvenlik, hizmet kalitesi, daha geniş adres alanı ve basitleştirilmiş, daha verimli başlık formatı elde etmiştir. Sonunda IPv4 üzerinde aşağıdaki iyileştirmeler yapıldı:
* Yeni Başlık Formatı: IPv6, IPv4 başlığındaki gereksiz alanları ortadan kaldırarak başlık formatını daha verimli hale getirir. Bu, ara yönlendiriciler için daha etkili bir performans sağlar.

* Genişletilebilirlik: IPv6 başlığı, başlık sonrasında eklenen uzantı başlıkları ile genişletilebilir bir yapıya sahiptir. Bu özellik, protokolün gelecekteki değişikliklere uyum sağlamasına olanak tanır.

* Geniş Adres Alanı: IPv6'nın 128-bitlik adres uzayı, daha fazla benzersiz IP adresi sağlar. Bu, birden fazla alt ağın oluşturulmasına ve adres tahsisinin daha etkili bir şekilde yapılmasına imkan tanır.

* Daha İyi Güvenlik: IPv6, IPSec'i standart olarak içerir ve başlık uzantıları aracılığıyla şifreleme ve kimlik doğrulama gibi güvenlik özelliklerini kolaylaştırır.

* SLAAC (Durum Bilgisi Olmayan ve Durum Bilgisi Olan Ana Bilgisayar Adresleme): DHCP sunucusu olmadığında, LAN'daki cihazlar otomatik olarak IP adreslerini alabilir ve ağı kullanmaya başlayabilir. Bu, ağ konfigürasyonunun daha esnek ve otomatik olmasını sağlar.(SLAAC, IPv6'nın bir özelliğidir ve IPv4 ile doğrudan karşılığı yoktur. IPv4 adresleri daha küçük bir uzaya sahiptir ve genellikle DHCP (Dynamic Host Configuration Protocol) kullanılarak yapılandırılır. DHCP, IPv4 cihazlarına dinamik olarak IP adresi, alt ağ maskesi, gateway adresi ve diğer konfigürasyon bilgilerini sağlayan bir protokoldür.)

* Daha Verimli LAN Etkileşimleri: IPv6, yayın tabanlı ARP protokolünü daha verimli ICMPv6 Komşu Keşfi mesajları ile değiştirir. Bu, ağ üzerindeki cihazların daha etkili bir şekilde iletişim kurmasını sağlar.(Ethernet segmentlerinde IPv4 kullanıldığında, katman 3'ten katman 2'ye eşleme olması gerekir; Ek olarak IPv4, adres çözümlemesini gerçekleştirmek için bir ARP yayını kullanır; bu, Ethernet bağlantı noktasında bir kesinti olarak işlenen bir Ethernet segmentindeki tüm istasyonlara gönderilen ve bu istasyonlar tarafından alınan bir ARP yayın paketini içerir.)

* Cihaz Başına Birden Fazla IPv6 Adresi: IPv6, bir cihazın aynı alt ağda birden fazla IPv6 adresine sahip olmasına izin verir. Bu, gelişmiş güvenlik, daha fazla gizlilik ve ek ağ özellikleri sağlar.

* Yeni Adres Türleri: IPv6 paketleri, yönlendirilemeyen IPv6 bağlantısı yerel adresleri gibi yeni ağ katmanı adres türlerini destekler. Bu, özel ağ senaryolarına uygunluk sağlar.
  
* Ağdaki her IPv6 düğümünün, yerel segmentinin dışında iletişim kurabilmesi için küresel olarak benzersiz bir adrese ihtiyacı vardır. Peki bir düğüm böyle bir adresi nereden alır? Birkaç seçenek var:

* Manuel Atama: Her düğüm, bir yönetici tarafından manuel olarak bir IPv6 adresiyle yapılandırılabilir. Ölçeklenebilir bir yaklaşım değildir ve insan hatasına açıktır. 

* DHCPv6 (Dinamik Ana Bilgisayar Yapılandırma Protokolü sürüm 6): Ana bilgisayarlara dinamik olarak adres atamak için en yaygın olarak benimsenen protokol. Ağda bir DHCP sunucusu ve ek yapılandırma gerektirir.

* SLAAC (Durum Bilgisi Olmayan Adres Otomatik Yapılandırması): IPv6 (Internet Protocol version 6) adres yapılandırmasında kullanılan bir protokoldür. Bu protokol, bilgisayarların ağa bağlandığında otomatik olarak IPv6 adreslerini yapılandırmalarını sağlar. Stateless (durumsuz) olarak adlandırılmasının sebebi, bu protokolün ağdaki diğer cihazlar veya bir merkezi sunucu tarafından yönetilen bir durum bilgisine ihtiyaç duymadan çalışabilmesidir.


## SLAAC Nedir
SLAAC, Durum Bilgisi Olmayan Adres Otomatik Yapılandırması anlamına gelir ve adı, ne yaptığını hemen hemen açıklar. Hangi adresin hangi düğüme atandığını herhangi bir cihazın takip etmesine gerek kalmadan, ağdaki her ana bilgisayarın benzersiz bir IPv6 adresini otomatik olarak yapılandırmasını sağlayan bir mekanizmadır.

* Durum bilgisi olan bir adres ataması, her atamanın durumunu izleyen bir sunucu veya başka bir cihazı içerir. Adres havuzunun kullanılabilirliğini izler ve yinelenen adres çakışmalarını çözer. Ayrıca her atamayı günlüğe kaydeder ve sona erme sürelerini takip eder.
  
* Durum bilgisi olmayan adres ataması,  hiçbir sunucunun hangi adreslerin atandığını ve bir atama için hangi adreslerin hâlâ kullanılabilir olduğunu takip edemediği anlamına gelir . Ayrıca durum bilgisi olmayan atama senaryosunda düğümler, şu mantığı izleyerek yinelenen adres çakışmalarını çözmekten sorumludur: Bir IPv6 adresi oluşturun, Yinelenen Adres Algılama'yı (DAD) çalıştırın, adres kullanımdaysa başka bir adres oluşturun ve DAD'yi yeniden çalıştırır.

## SLAAC Nasıl Çalışır
IPv6 otomatik adreslemenin nasıl çalıştığını tam olarak anlamak için, bir IPv6 düğümünün ağa bağlandığı andan benzersiz bir küresel tek noktaya yayın adresine sahip olduğu ana kadar attığı adımları izleyelim.

#### Adım 1: Düğüm Kendisini Yerel Bağlantı Adresiyle Yapılandırır
Bir IPv6 düğümü, IPv6 etkin bir ağa bağlandığında, genellikle yaptığı ilk şey, yerel bağlantı adresiyle kendisini otomatik olarak yapılandırmaktır. Bu yerel adresin amacı, düğümün Katman 3'te yerel segmentteki diğer IPv6 cihazlarıyla iletişim kurmasını sağlamaktır. Yerel bağlantı adresini otomatik olarak yapılandırmanın en yaygın olarak benimsenen yolu, yerel bağlantı öneki FE80::/64 ile arayüzün MAC adresinden oluşturulan EUI-64 arayüz tanımlayıcısının birleştirilmesidir.

IPv6'nın önemli özelliklerinden biri, yöneticinin yapılandırmasına gerek kalmadan otomatik adres atamasıdır. Bu, cihazların bir IPv6 bağlantısı üzerinden anında iletişim kurmasına olanak tanır. Bir cihaz, EUI-64 (IEEE Genişletilmiş Benzersiz Tanımlayıcı-64)  biçimini kullanarak kendisine otomatik olarak bir IPv6 adresi atayabilir. Bu adres, cihazın benzersiz 48 bitlik MAC adresinden oluşturulur. 48 bit bir IPv6 adresi oluşturmak için çok kısa olduğundan, ek onaltılık rakamlar eklenir. EUI-64, DHCP'ye veya manuel yapılandırmaya bağlı olmaksızın IPv6 adreslerinin otomatik yapılandırılmasına olanak tanır.
IPV6 16'lık sayı sistemi(hexadecimal numbering ) kullanır.Aşağıda hexadecimal numbering tablosu verilmiştir.

![hexadecimal](https://github.com/sumeyyaakbulut/IP/assets/62395974/798501e6-591b-466d-851a-69025ea46a13)


1. İlk adım 48 bit MAC adresini 64 bit değere dönüştürmektir. Bunu yapmak için MAC adresini 24 bitlik iki yarıya böleriz.24 bitlik bloklardan biri OUI (Organizationally UniqueIdentifier) olarak adlandırılır, diğeri ise ağ arayüz kartına özel olarak bilinir. Bu MAC tabanlı adres üretimi için IEEE tarafından ayrılmış 16 bitlik bir değer (0xFFFE) eklenir.("11111111 11111110" değerini (onaltılık sistemde "FFFE"))
   
2. IPV6 adresleme standartlarına göre, en soldaki 7. bit "Evrensel/Yerel" bit olarak adlandırılır. Bu bitin değeri 1 olarak ayarlanırsa, adres yerel olarak yapılandırılmıştır. Eğer bit değeri 0 ise, yönetilen adres global olarak adlandırılır.Manuel olarak yapılandırılmış bir MAC adresi gibi yerel olarak oluşturulan adresler de bu biti bire ayarlayacaktır.

Yukarıdaki maddelerde anlatılan içerikle ilgili örnek aşağıda gösterilmiştir.

![1](https://github.com/sumeyyaakbulut/IP/assets/62395974/6ab12451-5a47-4d3d-9a39-5f75ec3fd6a1)

#### Adım 2: Düğüm Yinelenen Adres Algılama (DAD) işlemini gerçekleştirir
IPv6 ana bilgisayarının yerel bağlantı adresi otomatik olarak yapılandırıldıktan sonra, adresin yerel segmentte gerçekten benzersiz olduğundan emin olması gerekir. Başka bir düğümün aynı adrese sahip olma ihtimali çok zayıf olmasına rağmen, Yinelenen Adres Algılama (DAD) adı verilen bir işlemi gerçekleştirmesi gerekir.

DAD, talep edilen düğüm çok noktaya yayın adı verilen özel bir adres türünü içeren bir mekanizmadır. Bir IPv6 adresi yapılandırıldıktan sonra her düğüm, FF02::1:FFxx:xxxx adresiyle tanımlanan bir çok noktaya yayın grubuna katılır; burada xx:xxxx, IPv6 tek noktaya yayın adresindeki son 6 (onaltılık) değerdir. Bu nedenle, yapılandırılmış her tek noktaya yayın adresi için, ister yerel bağlantı ister genel olsun, ana bilgisayar, ilgili otomatik olarak oluşturulan istenen düğüm çok noktaya yayın grubuna katılır.

Bu mantığı aklımızda bulundurarak, başka bir ana bilgisayarın aynı yerel bağlantı adresine sahip olması durumunda, bu adresten otomatik olarak oluşturulan istenen düğüm çok noktaya yayın grubundaki mesajları da dinleyeceğini biliyoruz - FF02::1:FF34:5678 . PC1'in bunu kontrol etmesi için hedef adresi bu gruba ve kaynak adresi IPv6 belirtilmemiş adresine ayarlanmış bir ICMPv6 mesajı gönderir. Paketin ICMPv6 bölümünde PC1, adresin tamamını Hedef Adres alanına koyar. Şekil 2 bu süreci göstermektedir. PC1 daha sonra paketi ağa gönderir. Yalnızca otomatik olarak oluşturulan bu çok noktaya yayın grubunu dinleyen düğümler paketi açacak, diğer tüm düğümler onu atacaktır. Herhangi bir düğümün son 6 (onaltılık) rakamı aynı olan bir IPv6 adresi varsa, ICMPv6 kısmına bakacak ve hedef adresin kendi adreslerinden herhangi biriyle eşleşip eşleşmediğini kontrol edecektir. Bir eşleşme varsa, ana bilgisayar bu IPv6 adresinin zaten kullanımda olduğuna yanıt verecektir. Kimse cevap vermezse, PC1 bu adresin benzersiz ve kullanıma uygun olduğu sonucuna varacak ve onu atayacaktır.

Bu işleme Yinelenen Adres Algılama (DAD) adı verilir ve her yeni adres atamasında gerçekleştirilir. Örneğimizde PC1, şekil 2'de gösterildiği gibi ICMPv6 Komşu Talep mesajını gönderiyor ve kimse yanıt vermiyor. PC1 daha sonra bu yerel bağlantı adresinin bu yerel segmentte benzersiz olduğundan emin olacaktır.

Adım 3: Düğüm bir Yönlendirici Talep mesajı gönderir
Bu örnekteki Adım 1 ve 2, benzersiz bir yerel bağlantı adresi oluşturma ve atama sürecini göstermektedir. Bu işlem tam olarak Durum Bilgisiz Otomatik Yapılandırma özelliğinin bir parçası değildir ancak yerel bağlantı adresi olmadan PC1, katman 3'te başka herhangi bir IPv6 düğümüyle iletişim kuramaz. Dolayısıyla SLAAC'ın çalışması için bir ön koşuldur ve bu yüzden onu örneğimize dahil ettik.

PC1 bir yerel bağlantı adresine sahip olduktan sonra artık SLAAC kullanarak global tek noktaya yayın adresini otomatik olarak yapılandırma işlemini başlatabilir. Bu sürecin ilk adımı Router Solicitation (RS) adı verilen bir ICMPv6 mesajı göndermektir. Bu mesajın amacı, bu segmente bağlı tüm IPv6 yönlendiricilerine, kullanılan genel tek noktaya yayın prefix hakkında sormaktır. Hedef adresi, tüm yönlendiricilerin çoklu yayın adresi FF02::2'dir ve kaynak için PC1, yerel bağlantı adresini kullanır. Yalnızca yönlendiricilerin FF02::2 çok noktaya yayın grubuna abone olduğunu unutmayın; bu, yalnızca Yönlendirici 1'in bu mesajı işleyeceği ve yerel segmentteki diğer tüm düğümlerin onu atacağı anlamına gelir.

Yönlendirici 1, Yönlendirici Talep mesajını aldıktan sonra, Yönlendirici Bildirisi (RA) adı verilen bir ICMPv6 mesajıyla yanıt verir. RA mesajı, bağlantıdaki genel IPv6 önekini ve önek uzunluğunu içerir. Örneğimizde bunlar 2001:1234:A:b:: öneki ve /64 önek uzunluğu olacaktır. Bu RA paketinin kaynağı için, Yönlendirici 1 kendi yerel bağlantı adresini kullanır ve hedef, tüm düğümlerin çoklu yayın adresi FF02::1'dir. İşlem şekil 3'te gösterilmektedir.

Adım 4: Düğüm genel tek noktaya yayın adresini yapılandırır
PC1, Yönlendirici 1'den Yönlendirici Bildirisini geri aldığında, 2001:1234:A:B::/64 önekini EUI-64 arabirim tanımlayıcısıyla (7207:12FF:FE34:5678) birleştirir ve sonuçta küresel tek noktaya yayın adresi 2001 elde edilir: 1234:A:B:7207:12FF:FE34:5678/64. Yönlendirici Bildirisi Yönlendirici 1'den geldiği için PC1, IPv6 varsayılan ağ geçidini R1'in yerel bağlantı adresine ayarlar.

Artık PC1'in küresel bir tek noktaya yayın adresi ve varsayılan bir ağ geçidi var. Ancak SLAAC süreci tamamlanmadı. PC1, otomatik olarak oluşturulan bu adresin yerel segmentte benzersiz olduğundan emin olmalıdır. Böylece PC1, Yinelenen Adres Tespiti (DAD) işlemini gerçekleştirir. 

Adım 5: Düğüm Yinelenen Adres Algılama (DAD) işlemini gerçekleştirir
DAD sürecini zaten 2. adımda ayrıntılı olarak açıklamıştık. PC1 global tek noktaya yayın adresini otomatik olarak oluşturduğunda, hemen otomatik olarak oluşturulan istenen düğüm çok noktaya yayın grubu FF02::1:FF34:5678'e katılır. Bu adresi başka kimsenin kullanmadığından emin olmak için PC1, talep edilen düğüm adresi FF02::1:FF34:5678'e Komşu Talep adı verilen bir ICMPv6 mesajı gönderir ve bir düğümün yanıt verip vermediğini görmek için bekler. Cevap alınmazsa PC1 bu adresin benzersiz olduğunu bilir ve bunu internet de dahil olmak üzere yerel segmenti dışında iletişim için kullanmaya başlayabilir.

SLAAC'la ilgili sorun
Bir düğümün küresel olarak benzersiz bir IPv6 adresini ve varsayılan ağ geçidini nasıl otomatik olarak yapılandırabildiğini gördük. Ancak SLAAC, DNS bilgisi sağlamaz ve DNS olmadan internette gezinmek gibi birçok hizmet mümkün değildir.  
Yönlendirici Reklamı başlığında bu sorunu çözmek için tasarlanmış bir alan bulunmaktadır.

Yönlendirici Reklam Bayrakları,yukarıda da söylediğimiz gibi SLAAC varsayılan olarak DNS sağlamaz. Ve DNS olmadan, URL adreslerinden IP'ye çözümleme gerektiren birçok hizmet çalışmayacaktır. RA mesajında, düğümlerin IPv6 adresini ve DNS bilgilerini nereden alabileceklerini anlamalarına yardımcı olan bir alan vardır. 

### IPv6 Header

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/d45e4e0a-9708-42ac-9b4f-0312dc3fdb9f)

### IPv4 Header

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/09616394-df1f-4620-82ed-161b7bee3e7d)

IPv6 Header:
* Version: Bu, pakette kullanılan IP tipini tanımlayan 4 bitlik bir alandır.
* Traffic Class: Bu 8 bitlik bir alandır. Bu, IPv4 başlığındaki Type Of Services alanına benzer. İlk 6 bit bu paket için gereken hizmeti temsil eder ve son 2 bit ECN (Açık Tıkanıklık Bildirimi) için kullanılır.
* Flow Label (20 bit): Bu etiket, bir iletişime ait paketlerin sıralı akışını sağlamak için kullanılır. Kaynak, yönlendiricinin belirli bir paketin belirli bir bilgi akışına ait olduğunu belirlemesine yardımcı olmak için diziyi etiketler. Bu alan veri paketlerinin yeniden sıralanmasını önlemeye yardımcı olur. Akış/gerçek zamanlı medya için tasarlanmıştır.
* Payload Length: IPv6 Yükü alanı, herhangi bir IPv6 Uzantısı başlığını içeren bir paketin veri bölümünün bayt cinsinden uzunluğunu belirten 16 bitlik bir tanımlayıcıdır. Buna karşılık, IPv4 Total Length alanı, IPv4 başlığı da dahil olmak üzere tüm IP paketinin uzunluğunu ölçer.
* Next Header: İlk uzantı başlığının türünü (varsa) veya veri yükündeki TCP, UDP veya ICMPv6 gibi üst katman protokolünü belirten 8 bitlik bir alandır. Alan, IPv4 Protokolü alanına benzer ancak bazı ek seçeneklere sahiptir. Bir üst katman protokolünü belirtirken IPv6 Sonraki Başlık alanı, IPv4 Protocol kullanılan değerlerin aynısını kullanır.
* Hop Limit (8-bit): Bu alan paketin ağda sonsuz döngüye girmesini durdurmak için kullanılır. Bu, IPv4'teki TTL ile aynıdır. Hop Limit alanının değeri, bir linkten (yönlendirici/atlama) geçerken 1 azaltılır. Alan 0'a ulaştığında paket atılır.
* Source Address (128 bit): Bu alan paketi oluşturanın adresini belirtir.
* Destination Address (128 bit): Bu alan, paketin hedeflenen alıcısının adresini sağlar.


### IPv6 Adres Türleri

#### 1. Unicast Addresses :
IPv6 (Unicast Addresses)Tek Noktaya Yayın Adresleri, tek bir arayüzü tanımlamak için kullanılır ve en yaygın IPv6 adresi türüdür. IPv6'daki tek noktaya yayın adresleri kapsamlarına ve amaçlarına göre çeşitli türlere ayrılabilir. IPv6 Tek Noktaya Yayın Adreslerinin ana türleri şunlardır:

##### 1.1. Global Unicast Address
* Format: Global Tek Noktaya Yayın Adresleri prefix ile başlar 2000::/3.
* Kapsam: İnternette küresel olarak yönlendirilebilir.
* Amacı: Küresel İnternet üzerinde uçtan uca iletişim için kullanılır. Genel IPv4 adreslerine benzer.

##### 1.2. Link-Local Address:
* Format: Bağlantı-Yerel Adresler prefixi ile başlar fe80::/10.
* Kapsam: Yerel ağ segmentiyle sınırlıdır.
* Amaç: Tek bir ağ segmentinde iletişim için kullanılır. Yerel bağlantı adresleri otomatik olarak yapılandırılır ve genel bir adres gerektirmez. Genellikle komşu keşfi ve otomatik yapılandırma için kullanılırlar.

##### 1.3. Unique Local Unicast Address (ULA):
* Format: Benzersiz Yerel Adresler prefixi ile başlar fc00::/7.
* Kapsam: Bir kuruluş veya sitenin yereli.
* Amaç: Bir site veya kuruluş içinde yerel iletişim için kullanılan IPv4 özel adreslerine benzer. Küresel İnternet üzerinde yönlendirilemez.

##### 1.4. Loopback Address:
* Format: Geridöngü adresi ::1/128.
* Kapsam: Cihazın yereli.
* Amaç: Yerel cihazdaki iletişimi test etmek için kullanılan IPv4 127.0.0.1'e eşdeğerdir. Bir cihazın ağ arayüzü kullanmadan paket gönderip almasına olanak tanır.

#### 2. Multicast Addresses :
Ağ çok noktaya yayın, bir düğümün paketleri aynı anda birden çok hedefe (birden çoğa) gönderdiği bir tekniktir. Hedefler aslında  çok noktaya yayın grubu olarak bilinen tek bir çok noktaya yayın adresiyle tanımlanan bir dizi arabirimdir.

IPv6'da çok noktaya yayın adresleri, adreslerin en soldaki 8 bitinin değeriyle diğer tüm türlerden ayrılır: 11111111 değeri (onaltılık basamak FF), adresin çok noktaya yayın olduğunu tanımlar. Bu nedenle, tüm çok noktaya yayın adresleri, 224.0.0.0/4 IPv4 çok noktaya yayın adres alanına eşdeğer olan ff00::/8 önekinin bir parçasıdır. IPv4 ve IPv6 çok noktaya yayın için iki önemli kural geçerlidir:
Çok noktaya yayın grubuna gönderilen paketlerin her zaman tek noktaya yayın kaynak adresi vardır.
Çok noktaya yayın adresi bir paketin kaynak adresi olamaz.
IPv6'da yayın adresleri yoktur. Bunun yerine, IPv6'da bu işlevsellik, tüm IPv6 aygıtlarının çok noktaya yayın adresi ve istenen düğüm çok noktaya yayın adresi gibi özel çok noktaya yayın grupları kullanılarak yapılır.

#### 2.1. Well-Known
IPv4'te 224.0.0.0/24 aralığında iyi bilinen birkaç çok noktaya yayın adresi vardır. İyi bilinen, bu adreslerin önceden tanımlanmış ve özel kullanım için ayrılmış olduğu anlamına gelir.

IPv6'da tüm bilinen çok noktaya yayın adresleri ff00::/12 önekiyle başlar. Bu, bir adresin onaltılık tabandaki ilk 3 rakamının her zaman ff0 olacağı anlamına gelir. Bu tür adreslerin birkaç örneği aşağıdaki tabloda gösterilmektedir:

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/2af9ef74-bd50-4194-ad9a-df767bcd110b)

#### 2.2. Solicited-Node :
İstenen Düğüm Çok Noktaya Yayın Adresi, etkili adres çözümlemesi için IPv6'da kullanılan özel bir çok noktaya yayın adresi türüdür. IPv6'da, IPv4'te kullanılan Adres Çözümleme Protokolü'nün (ARP), Komşu Keşif Protokolü (NDP) ile değiştirilmiştir. İstenen Düğüm Çok Noktaya Yayın Adresleri, bir hedef düğümün bağlantı katmanı adresini verimli bir şekilde çözmek için Komşu Keşif sürecinde kullanılır.

İstenen Düğüm Çok Noktaya Yayın Adresinin formatı, bir IPv6 tek noktaya yayın veya herhangi bir noktaya yayın adresinin son 24 bitinden türetilir. İstenen Düğüm Çok Noktaya Yayın Adresinin öneki şeklindedir ff02:0:0:0:0:1:ff00::/104ve son 24 bit, hedef tek noktaya yayın veya herhangi bir noktaya yayın adresinden alınır.


### Neighbor Discovery Protocol
IPv6'da Adres Çözümleme Protokolü (ARP) yoktur. IPv6'dan MAC'a çözümlemenin nasıl yapılıyor? IPv6 Komşu Keşif Protokolü (Neighbor Discovery Protocol), IPv4'teki ARP'ye benzer bir rol oynar, ancak daha gelişmiş ve güvenli bir şekilde çalışır. IPv6'da ARP'nin yerini alan bu protokol, düğümlerin birbirlerinin fiziksel adreslerini çözümlemek için kullanılır. İşte IPv6 Komşu Keşif Protokolü'nün temel adımları:

* Neighbor Solicitation (Komşu İsteme): Bir düğüm, bilmediği bir IPv6 adresinin MAC (Medya Erişim Kontrolü) adresini öğrenmek istediğinde, bu bilgiyi elde etmek amacıyla "Neighbor Solicitation" (NS) mesajı gönderir.
  
* Neighbor Advertisement (Komşu Bildirimi): Hedef IPv6 adresine sahip düğüm, NS mesajını alır ve kendi MAC adresini içeren "Neighbor Advertisement" (NA) mesajını gönderir. Bu, çözümleme sürecinin bir parçasıdır.
  
* Duplicate Address Detection (Adres Çakışması Algılama): IPv6'da, bir düğüm bir IPv6 adresini kullanmadan önce, bu adresin kullanımda olup olmadığını belirlemek için "Duplicate Address Detection" (DAD) sürecini yürütür. Bu, adresin benzersiz olup olmadığını kontrol etmek için NS ve NA mesajlarını içerir.
  
* Router Solicitation (Yönlendirici İsteme) ve Router Advertisement (Yönlendirici Bildirimi): Düğümler, ağdaki yönlendiricileri keşfetmek ve ağ yapılandırması bilgilerini almak için "Router Solicitation" (RS) ve "Router Advertisement" (RA) mesajlarını kullanabilirler.
  
* Redirect (Yönlendir): Bir yönlendirici, bir düğümün belirli bir hedefe daha iyi bir yol bulması durumunda, "Redirect" mesajını kullanarak düğümü yeni bir yol üzerinden yönlendirebilir.
  
* Multicast Kullanımı: IPv6 Komşu Keşif Protokolü, yayın yerine "Multicast" mesajlarını kullanarak iletişim kurar. Bu, ağ trafiğini düşük seviyede tutar ve daha etkin bir çözümleme süreci sağlar.
