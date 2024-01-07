# IPv6
IPv6(İnternet Protokolü) Sürüm 6, iletişimin ağ üzerinden gerçekleşmesine izin veren bir ağ katmanı protokolüdür.

## EUI-64 Adresleme
IPv6'nın önemli özelliklerinden biri, yöneticinin yapılandırmasına gerek kalmadan otomatik adres atamasıdır. Bu, cihazların bir IPv6 bağlantısı üzerinden anında iletişim kurmasına olanak tanır. Bir cihaz, EUI-64 (IEEE Genişletilmiş Benzersiz Tanımlayıcı-64)  biçimini kullanarak kendisine otomatik olarak bir IPv6 adresi atayabilir. Bu adres, cihazın benzersiz 48 bitlik MAC adresinden oluşturulur. 48 bit bir IPv6 adresi oluşturmak için çok kısa olduğundan, ek onaltılık rakamlar eklenir. EUI-64, DHCP'ye veya manuel yapılandırmaya bağlı olmaksızın IPv6 adreslerinin otomatik yapılandırılmasına olanak tanır.

1. İlk adım 48 bit MAC adresini 64 bit değere dönüştürmektir. Bunu yapmak için MAC adresini 24 bitlik iki yarıya böleriz:


![hexadecimal](https://github.com/sumeyyaakbulut/IP/assets/62395974/798501e6-591b-466d-851a-69025ea46a13)
