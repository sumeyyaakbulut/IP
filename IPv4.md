# IPv4
IP, İnternet Protokolü anlamına gelir ve v4, Sürüm Dört (IPv4) anlamına gelir. Bir IP adresi 32 bittir ve network kısmı ve host bilgisayar kısmı olmak üzere 2 bölümden oluşur.IP adresi 32 bittir ancak biz onu 8 bitlik 4 blok halinde yazıyoruz. 

Network kısmı bize IP adresinin hangi “ağa” ait olacağını söyleyecektir, bunu bir telefon numarasının şehir veya alan koduyla karşılaştırabilirsiniz. Host (Ana bilgisayar) kısmı ağ cihazını benzersiz şekilde tanımlar; bunlar telefon numaranızın son rakamları gibidir.

Yerel ağlarda çoğunlukla kullanılan 192.168.1.1 ip adresinin ilk 3 byte network, son byte ise host gösterir.Ama neden ilk 3 byte network kısmı ve neden son byte host dedik?
IP adresimiz 192.168.1.1, 255.255.255.0 alt ağ maskesiyle birlikte gelir. Alt ağ maskesi(subnet mask) bilgisayarınıza hangi bölümün “network” bölümü, hangisinin “host” bölümü olduğunu söyler. İsmine rağmen hiçbir şeyi “saklamaz” veya “maskelemez”.

### IPv4'ün Özellikleri
* IPv4, 32 Bitlik bir IP Adresi olabilir.
* IPv4 sayısal bir adres olabilir ve bitleri bir noktayla ayrılmıştır.
* Başlık alanlarının sayısı on iki, başlık alanının uzunluğu ise yirmidir.
* Tek noktaya yayın, yayın ve çok noktaya yayın tarzı adreslere sahiptir.
* IPv4, VLSM'yi (Sanal Uzunluk Alt Ağ Maskesi) destekler.
* IPv4, MAC adresini eşleştirmek için Posta Adresi Çözümleme Protokolünü kullanır.
* RIP, yönlendirilen arka plan programı tarafından desteklenen bir yönlendirme protokolü olabilir.
* Ağların manuel olarak veya DHCP ile tasarlanması gerekmektedir.
* Paket parçalanmasına yönlendiricilerden ve ana bilgisayardan izin veriliyor.

IPv4 paketine göz atalım:

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/b71354c1-cf45-4c69-924f-a89310d1fa88)

Protocol: Burada IP'nin yanı sıra hangi protokolü kullandığımızı bulacaksınız. Hangi aktarım katmanı protokolünü kullandığımızı bu şekilde belirleriz. Yani burada TCP, UDP veya belki başka bir şey bulacaksınız.
Source Address: Burada bu IP paketini oluşturan cihazın IP adresini bulunur.
Destination Address: IP paketini alması gereken cihazın IP adresidir.

IP adresine 8 bitlik bloklara gösterimi aşağıdadır.
![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/eeb8350c-81a8-4ec9-aee6-94f63c9ba8ad)

IP Adresi sınıfları içerir. Genel olarak, IPv4 Adresleme sistemi beş IP Adresi sınıfına bölünmüştür. Beş sınıfın tamamı IP Adresinin ilk sekizlisiyle tanımlanır.

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/c571e003-7623-4fd7-bb81-5c5fac832263)

* A Sınıfı: İlk bit her zaman 0 olmalıdır.
* B Sınıf : İlk 2 bit her zaman 10 olmalıdır.
* C Sınıfı: İlk 3 bit her zaman 110 olmalıdır.
* D Sınıfı: ilk sekizlinin ilk dört biti 1110 olmalıdır.
* 
Peki sahip olduğumuz aralıklar tam olarak nedir?

* A Sınıfı: 0.0.0.0 –   126.255.255.255
* B Sınıfı: 128.0.0.0 – 191.255.255.255
* C Sınıfı: 192.0.0.0 – 223.255.255.255
* D Sınıfı: 224.0.0.0 - 239.255.255.255
* E Sınıfı: 240.0.0.0 - 255.255.255.254

### IPv4'ün Bölümleri
#### Network Kısmı : Ağ kısmı, ağa atanan ayırt edici çeşitliliği belirtir. Ağ kısmı, atanan ağın kategorisini birlikte tanımlar.
#### Host Part: Ana bilgisayar parçası, ağınızdaki makineyi benzersiz şekilde tanımlar. IPv4 adresinin bu kısmı her ana bilgisayara atanır. 
Ağdaki her ana bilgisayar için ağ kısmı aynıdır ancak ana bilgisayarın yarısı farklılık göstermelidir.
#### Alt ağ numarası: Bu IPv4'ün zorunlu olmayan kısmıdır. Çok sayıda ana bilgisayara sahip yerel ağlar, alt ağlara bölünür ve bunlara alt ağ numaraları atanır.
