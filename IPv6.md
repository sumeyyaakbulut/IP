# IPv6
IPv6(İnternet Protokolü) Sürüm 6, iletişimin ağ üzerinden gerçekleşmesine izin veren bir ağ katmanı protokolüdür.IPv4, internet protokolü dünyasında bir dönüm noktası olmuş ve milyarlarca cihazın birbirine bağlanmasını mümkün kılan 32 bitlik bir adresleme sistemini tanıtmıştır. Ancak, IPv4'ün kullanılabilir adres sayısı sınırlıdır ve bu durum, internetin hızla büyümesiyle birlikte ciddi bir sorun haline gelmiştir. IPv4, toplamda 4.294.967.295 adet (yaklaşık 4.3 milyar) IP adresi sağlayabilir. 

Başlangıçta, A, B ve C sınıfı adres aralıkları ile farklı büyüklükteki ağlara IP adresi ataması yapılıyordu. Örneğin, C sınıfı 256 IP adresi, B sınıfı 65.535 IP adresi ve A sınıfı 16.777.216 IP adresi sağlardı. Büyük şirketler, özellikle A sınıfı ağları kullanarak milyonlarca IP adresine sahip oldular. Ancak, bu büyük blokların birçoğu tam anlamıyla kullanılmadı ve birçok IP adresi boşa harcandı.

Değişken Uzunluklu Alt Ağ Maskesi (VLSM) ve Network Address Translation (NAT) gibi teknolojiler, IP adreslerini daha etkili bir şekilde kullanmamıza yardımcı oldu. VLSM, istediğimiz alt ağ maskesini kullanarak daha küçük alt ağlar oluşturmamıza izin verdi. NAT ve Port Address Translation (PAT) ise bir genel IP adresinin arkasında birçok özel IP adresini paylaşmamıza olanak tanıdı.

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
  
Ağdaki her IPv6 düğümünün, yerel segmentinin dışında iletişim kurabilmesi için küresel olarak benzersiz bir adrese ihtiyacı vardır. Peki bir düğüm böyle bir adresi nereden alır? Birkaç seçenek var:

Manuel Atama: Her düğüm, bir yönetici tarafından manuel olarak bir IPv6 adresiyle yapılandırılabilir. Ölçeklenebilir bir yaklaşım değildir ve insan hatasına açıktır. 

DHCPv6 (Dinamik Ana Bilgisayar Yapılandırma Protokolü sürüm 6): Ana bilgisayarlara dinamik olarak adres atamak için en yaygın olarak benimsenen protokol. Ağda bir DHCP sunucusu ve ek yapılandırma gerektirir.

SLAAC (Durum Bilgisi Olmayan Adres Otomatik Yapılandırması): IPv6 (Internet Protocol version 6) adres yapılandırmasında kullanılan bir protokoldür. Bu protokol, bilgisayarların ağa bağlandığında otomatik olarak IPv6 adreslerini yapılandırmalarını sağlar. Stateless (durumsuz) olarak adlandırılmasının sebebi, bu protokolün ağdaki diğer cihazlar veya bir merkezi sunucu tarafından yönetilen bir durum bilgisine ihtiyaç duymadan çalışabilmesidir.


## SLAAC Nedir
SLAAC, Durum Bilgisi Olmayan Adres Otomatik Yapılandırması anlamına gelir ve adı, ne yaptığını hemen hemen açıklar. Hangi adresin hangi düğüme atandığını herhangi bir cihazın takip etmesine gerek kalmadan, ağdaki her ana bilgisayarın benzersiz bir IPv6 adresini otomatik olarak yapılandırmasını sağlayan bir mekanizmadır.

* Durum bilgisi olan bir adres ataması, her atamanın durumunu izleyen bir sunucu veya başka bir cihazı içerir. Adres havuzunun kullanılabilirliğini izler ve yinelenen adres çakışmalarını çözer. Ayrıca her atamayı günlüğe kaydeder ve sona erme sürelerini takip eder.
  
* Durum bilgisi olmayan adres ataması,  hiçbir sunucunun hangi adreslerin atandığını ve bir atama için hangi adreslerin hâlâ kullanılabilir olduğunu takip edemediği anlamına gelir . Ayrıca durum bilgisi olmayan atama senaryosunda düğümler, şu mantığı izleyerek yinelenen adres çakışmalarını çözmekten sorumludur: Bir IPv6 adresi oluşturun, Yinelenen Adres Algılama'yı (DAD) çalıştırın, adres kullanımdaysa başka bir adres oluşturun ve DAD'yi yeniden çalıştırın. , vesaire.

## SLAAC Nasıl Çalışır
IPv6 otomatik adreslemenin nasıl çalıştığını tam olarak anlamak için, bir IPv6 düğümünün ağa bağlandığı andan benzersiz bir küresel tek noktaya yayın adresine sahip olduğu ana kadar attığı adımları izleyelim.

Adım 1: Düğüm kendisini yerel bağlantı adresiyle yapılandırır
Bir IPv6 düğümü, IPv6 etkin bir ağa bağlandığında, genellikle yaptığı ilk şey, yerel bağlantı adresiyle kendisini otomatik olarak yapılandırmaktır. Bu yerel adresin amacı, düğümün Katman 3'te yerel segmentteki diğer IPv6 cihazlarıyla iletişim kurmasını sağlamaktır. Yerel bağlantı adresini otomatik olarak yapılandırmanın en yaygın olarak benimsenen yolu, yerel bağlantı öneki FE80::/64 ile arayüzün MAC adresinden oluşturulan EUI-64 arayüz tanımlayıcısının birleştirilmesidir.

IPv6'nın önemli özelliklerinden biri, yöneticinin yapılandırmasına gerek kalmadan otomatik adres atamasıdır. Bu, cihazların bir IPv6 bağlantısı üzerinden anında iletişim kurmasına olanak tanır. Bir cihaz, EUI-64 (IEEE Genişletilmiş Benzersiz Tanımlayıcı-64)  biçimini kullanarak kendisine otomatik olarak bir IPv6 adresi atayabilir. Bu adres, cihazın benzersiz 48 bitlik MAC adresinden oluşturulur. 48 bit bir IPv6 adresi oluşturmak için çok kısa olduğundan, ek onaltılık rakamlar eklenir. EUI-64, DHCP'ye veya manuel yapılandırmaya bağlı olmaksızın IPv6 adreslerinin otomatik yapılandırılmasına olanak tanır.
IPV6 16'lık sayı sistemi(hexadecimal numbering ) kullanır.Aşağıda hexadecimal numbering tablosu verilmiştir.

![hexadecimal](https://github.com/sumeyyaakbulut/IP/assets/62395974/798501e6-591b-466d-851a-69025ea46a13)


1. İlk adım 48 bit MAC adresini 64 bit değere dönüştürmektir. Bunu yapmak için MAC adresini 24 bitlik iki yarıya böleriz.24 bitlik bloklardan biri OUI (Organizationally UniqueIdentifier) olarak adlandırılır, diğeri ise ağ arayüz kartına özel olarak bilinir. Bu MAC tabanlı adres üretimi için IEEE tarafından ayrılmış 16 bitlik bir değer (0xFFFE) eklenir.("11111111 11111110" değerini (onaltılık sistemde "FFFE"))
   
2. IPV6 adresleme standartlarına göre, en soldaki 7. bit "Evrensel/Yerel" bit olarak adlandırılır. Bu bitin değeri 1 olarak ayarlanırsa, adres yerel olarak yapılandırılmıştır. Eğer bit değeri 0 ise, yönetilen adres global olarak adlandırılır.Manuel olarak yapılandırılmış bir MAC adresi gibi yerel olarak oluşturulan adresler de bu biti bire ayarlayacaktır.

Yukarıdaki maddelerde anlatılan içerikle ilgili örnek aşağıda gösterilmiştir.

![1](https://github.com/sumeyyaakbulut/IP/assets/62395974/6ab12451-5a47-4d3d-9a39-5f75ec3fd6a1)


