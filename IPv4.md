# IPv4
IP, İnternet Protokolü anlamına gelir ve v4, Sürüm Dört (IPv4) anlamına gelir. Bir IP adresi 32 bittir ve network kısmı ve host bilgisayar kısmı olmak üzere 2 bölümden oluşur.IP adresi 32 bittir ancak biz onu 8 bitlik 4 blok halinde yazıyoruz. 

Network kısmı bize IP adresinin hangi “ağa” ait olacağını söyleyecektir, bunu bir telefon numarasının şehir veya alan koduyla karşılaştırabilirsiniz. Host (Ana bilgisayar) kısmı ağ cihazını benzersiz şekilde tanımlar; bunlar telefon numaranızın son rakamları gibidir.

Yerel ağlarda çoğunlukla kullanılan 192.168.1.1 ip adresinin ilk 3 byte network, son byte ise host gösterir.Ama neden ilk 3 byte network kısmı ve neden son byte host dedik?
IP adresimiz 192.168.1.1, 255.255.255.0 alt ağ maskesiyle birlikte gelir. Alt ağ maskesi(subnet mask) bilgisayarınıza hangi bölümün “network” bölümü, hangisinin “host” bölümü olduğunu söyler. İsmine rağmen hiçbir şeyi “saklamaz” veya “maskelemez”.


### IPv4'ün Bölümleri
#### Network Kısmı : Ağ kısmı, ağa atanan ayırt edici çeşitliliği belirtir. Ağ kısmı, atanan ağın kategorisini birlikte tanımlar.
#### Host Part: Ana bilgisayar parçası, ağınızdaki makineyi benzersiz şekilde tanımlar. IPv4 adresinin bu kısmı her ana bilgisayara atanır. 
Ağdaki her ana bilgisayar için ağ kısmı aynıdır ancak ana bilgisayarın yarısı farklılık göstermelidir.
#### Alt ağ numarası: Bu IPv4'ün zorunlu olmayan kısmıdır. Çok sayıda ana bilgisayara sahip yerel ağlar, alt ağlara bölünür ve bunlara alt ağ numaraları atanır.
