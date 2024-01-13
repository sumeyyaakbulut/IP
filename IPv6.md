# IPv6
IPv6(İnternet Protokolü) Sürüm 6, iletişimin ağ üzerinden gerçekleşmesine izin veren bir ağ katmanı protokolüdür.IPv4, internet protokolü dünyasında bir dönüm noktası olmuş ve milyarlarca cihazın birbirine bağlanmasını mümkün kılan 32 bitlik bir adresleme sistemini tanıtmıştır. Ancak, IPv4'ün kullanılabilir adres sayısı sınırlıdır ve bu durum, internetin hızla büyümesiyle birlikte ciddi bir sorun haline gelmiştir. IPv4, toplamda 4.294.967.295 adet (yaklaşık 4.3 milyar) IP adresi sağlayabilir. 
Başlangıçta, A, B ve C sınıfı adres aralıkları ile farklı büyüklükteki ağlara IP adresi ataması yapılıyordu. Örneğin, C sınıfı 256 IP adresi, B sınıfı 65.535 IP adresi ve A sınıfı 16.777.216 IP adresi sağlardı. Büyük şirketler, özellikle A sınıfı ağları kullanarak milyonlarca IP adresine sahip oldular. Ancak, bu büyük blokların birçoğu tam anlamıyla kullanılmadı ve birçok IP adresi boşa harcandı.
Değişken Uzunluklu Alt Ağ Maskesi (VLSM) ve Network Address Translation (NAT) gibi teknolojiler, IP adreslerini daha etkili bir şekilde kullanmamıza yardımcı oldu. VLSM, istediğimiz alt ağ maskesini kullanarak daha küçük alt ağlar oluşturmamıza izin verdi. NAT ve Port Address Translation (PAT) ise bir genel IP adresinin arkasında birçok özel IP adresini paylaşmamıza olanak tanıdı.
Ancak, internetin hızlı büyümesi ve cihaz sayısındaki patlama, bu önlemlerin sınırlarını zorladı. VLSM ve NAT/PAT gibi çözümlere rağmen, IPv6'nın getirdiği 128 bitlik adresleme sistemi (2^128 sayısı yani 340 undecilyon civarında IP adresi sağlayabilir), çok daha geniş bir adresleme alanı sağlayarak gelecekteki büyüme ve genişleme ihtiyaçlarına cevap vermeyi hedefler. IPv6, internetin daha sürdürülebilir ve genişletilebilir olmasını sağlamak için önemli bir adımdır.

## IPv6 Adres Gösterimi


## EUI-64 Adresleme
IPv6'nın önemli özelliklerinden biri, yöneticinin yapılandırmasına gerek kalmadan otomatik adres atamasıdır. Bu, cihazların bir IPv6 bağlantısı üzerinden anında iletişim kurmasına olanak tanır. Bir cihaz, EUI-64 (IEEE Genişletilmiş Benzersiz Tanımlayıcı-64)  biçimini kullanarak kendisine otomatik olarak bir IPv6 adresi atayabilir. Bu adres, cihazın benzersiz 48 bitlik MAC adresinden oluşturulur. 48 bit bir IPv6 adresi oluşturmak için çok kısa olduğundan, ek onaltılık rakamlar eklenir. EUI-64, DHCP'ye veya manuel yapılandırmaya bağlı olmaksızın IPv6 adreslerinin otomatik yapılandırılmasına olanak tanır.
IPV6 16'lık sayı sistemi(hexadecimal numbering ) kullanır.Aşağıda hexadecimal numbering tablosu verilmiştir.

![hexadecimal](https://github.com/sumeyyaakbulut/IP/assets/62395974/798501e6-591b-466d-851a-69025ea46a13)


1. İlk adım 48 bit MAC adresini 64 bit değere dönüştürmektir. Bunu yapmak için MAC adresini 24 bitlik iki yarıya böleriz.24 bitlik bloklardan biri OUI (Organizationally UniqueIdentifier) olarak adlandırılır, diğeri ise ağ arayüz kartına özel olarak bilinir. Bu MAC tabanlı adres üretimi için IEEE tarafından ayrılmış 16 bitlik bir değer (0xFFFE) eklenir.("11111111 11111110" değerini (onaltılık sistemde "FFFE"))
   
2. IPV6 adresleme standartlarına göre, en soldaki 7. bit "Evrensel/Yerel" bit olarak adlandırılır. Bu bitin değeri 1 olarak ayarlanırsa, adres yerel olarak yapılandırılmıştır. Eğer bit değeri 0 ise, yönetilen adres global olarak adlandırılır.Manuel olarak yapılandırılmış bir MAC adresi gibi yerel olarak oluşturulan adresler de bu biti bire ayarlayacaktır.

Yukarıdaki maddelerde anlatılan içerikle ilgili örnek aşağıda gösterilmiştir.

![1](https://github.com/sumeyyaakbulut/IP/assets/62395974/6ab12451-5a47-4d3d-9a39-5f75ec3fd6a1)


