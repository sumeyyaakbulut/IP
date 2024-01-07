# IPv6
IPv6(İnternet Protokolü) Sürüm 6, iletişimin ağ üzerinden gerçekleşmesine izin veren bir ağ katmanı protokolüdür.

## EUI-64 Adresleme
IPv6'nın önemli özelliklerinden biri, yöneticinin yapılandırmasına gerek kalmadan otomatik adres atamasıdır. Bu, cihazların bir IPv6 bağlantısı üzerinden anında iletişim kurmasına olanak tanır. Bir cihaz, EUI-64 (IEEE Genişletilmiş Benzersiz Tanımlayıcı-64)  biçimini kullanarak kendisine otomatik olarak bir IPv6 adresi atayabilir. Bu adres, cihazın benzersiz 48 bitlik MAC adresinden oluşturulur. 48 bit bir IPv6 adresi oluşturmak için çok kısa olduğundan, ek onaltılık rakamlar eklenir. EUI-64, DHCP'ye veya manuel yapılandırmaya bağlı olmaksızın IPv6 adreslerinin otomatik yapılandırılmasına olanak tanır.
IPV6 16'lık sayı sistemi(hexadecimal numbering ) kullanır.Aşağıda hexadecimal numbering tablosu verilmiştir.

![hexadecimal](https://github.com/sumeyyaakbulut/IP/assets/62395974/798501e6-591b-466d-851a-69025ea46a13)


1. İlk adım 48 bit MAC adresini 64 bit değere dönüştürmektir. Bunu yapmak için MAC adresini 24 bitlik iki yarıya böleriz.
   
2. IPV6 adresleme standartlarına göre, en soldaki 7. bit "Evrensel/Yerel" bit olarak adlandırılır. Bu bitin değeri 1 olarak ayarlanırsa, adres yerel olarak yapılandırılmıştır. Eğer bit değeri 0 ise, yönetilen adres global olarak adlandırılır.Manuel olarak yapılandırılmış bir MAC adresi gibi yerel olarak oluşturulan adresler de bu biti bire ayarlayacaktır.



![1](https://github.com/sumeyyaakbulut/IP/assets/62395974/6ab12451-5a47-4d3d-9a39-5f75ec3fd6a1)


