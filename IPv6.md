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

* SLAAC (Durum Bilgisi Olmayan ve Durum Bilgisi Olan Ana Bilgisayar Adresleme): DHCP sunucusu olmadığında, LAN'daki cihazlar otomatik olarak IP adreslerini alabilir ve ağı kullanmaya başlayabilir. Bu, ağ konfigürasyonunun daha esnek ve otomatik olmasını sağlar.

* Daha Verimli LAN Etkileşimleri: IPv6, yayın tabanlı ARP protokolünü daha verimli ICMPv6 Komşu Keşfi mesajları ile değiştirir. Bu, ağ üzerindeki cihazların daha etkili bir şekilde iletişim kurmasını sağlar.

* Cihaz Başına Birden Fazla IPv6 Adresi: IPv6, bir cihazın aynı alt ağda birden fazla IPv6 adresine sahip olmasına izin verir. Bu, gelişmiş güvenlik, daha fazla gizlilik ve ek ağ özellikleri sağlar.

* Yeni Adres Türleri: IPv6 paketleri, yönlendirilemeyen IPv6 bağlantısı yerel adresleri gibi yeni ağ katmanı adres türlerini destekler. Bu, özel ağ senaryolarına uygunluk sağlar.

## IPv6 Adres Gösterimi


## EUI-64 Adresleme
IPv6'nın önemli özelliklerinden biri, yöneticinin yapılandırmasına gerek kalmadan otomatik adres atamasıdır. Bu, cihazların bir IPv6 bağlantısı üzerinden anında iletişim kurmasına olanak tanır. Bir cihaz, EUI-64 (IEEE Genişletilmiş Benzersiz Tanımlayıcı-64)  biçimini kullanarak kendisine otomatik olarak bir IPv6 adresi atayabilir. Bu adres, cihazın benzersiz 48 bitlik MAC adresinden oluşturulur. 48 bit bir IPv6 adresi oluşturmak için çok kısa olduğundan, ek onaltılık rakamlar eklenir. EUI-64, DHCP'ye veya manuel yapılandırmaya bağlı olmaksızın IPv6 adreslerinin otomatik yapılandırılmasına olanak tanır.
IPV6 16'lık sayı sistemi(hexadecimal numbering ) kullanır.Aşağıda hexadecimal numbering tablosu verilmiştir.

![hexadecimal](https://github.com/sumeyyaakbulut/IP/assets/62395974/798501e6-591b-466d-851a-69025ea46a13)


1. İlk adım 48 bit MAC adresini 64 bit değere dönüştürmektir. Bunu yapmak için MAC adresini 24 bitlik iki yarıya böleriz.24 bitlik bloklardan biri OUI (Organizationally UniqueIdentifier) olarak adlandırılır, diğeri ise ağ arayüz kartına özel olarak bilinir. Bu MAC tabanlı adres üretimi için IEEE tarafından ayrılmış 16 bitlik bir değer (0xFFFE) eklenir.("11111111 11111110" değerini (onaltılık sistemde "FFFE"))
   
2. IPV6 adresleme standartlarına göre, en soldaki 7. bit "Evrensel/Yerel" bit olarak adlandırılır. Bu bitin değeri 1 olarak ayarlanırsa, adres yerel olarak yapılandırılmıştır. Eğer bit değeri 0 ise, yönetilen adres global olarak adlandırılır.Manuel olarak yapılandırılmış bir MAC adresi gibi yerel olarak oluşturulan adresler de bu biti bire ayarlayacaktır.

Yukarıdaki maddelerde anlatılan içerikle ilgili örnek aşağıda gösterilmiştir.

![1](https://github.com/sumeyyaakbulut/IP/assets/62395974/6ab12451-5a47-4d3d-9a39-5f75ec3fd6a1)


