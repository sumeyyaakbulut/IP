### IPv4 Nedir
IP, İnternet Protokolü'nü temsil eder ve IPv4, Sürüm Dört anlamına gelir.Bir IPv4 adresi 32 bittir ve network ve host kısmı olmak üzere 2 bölümden oluşur. IPv4 32, 8 bitlik 4 blok halinde yazılır.

### IPv4 Yapısı
IP adresi, iki temel bileşen içerir: network (ağ) kısmı ve host (ana bilgisayar) kısmı. Network kısmı, IP adresinin hangi ağa ait olduğunu belirtir ve bu, telefon numarasının şehir veya alan koduna benzetilebilir. Host kısmı ise ağdaki cihazı benzersiz bir şekilde tanımlar, bu da telefon numarasının son rakamlarına benzetilebilir

### Alt Ağ Maskesi(Subnet Mask)
Örneğin, yerel ağlarda yaygın olarak kullanılan 192.168.1.1 IP adresi, 255.255.255.0 alt ağ maskesiyle birlikte gelir.

Bu IP adresinin ilk 3 byte'ı (24 bit) "network" kısmını temsil eder. Bu kısım, cihazın hangi ağa ait olduğunu belirtir ve genellikle tüm cihazlar aynı ağ içerisinde bulunur. Bu benzetmeye telefon numarası örneğinden devam edecek olursak, ilk 3 byte, bir şehir veya bölge kodunu temsil eder.

Son byte (8 bit), ise "host" kısmını temsil eder. Bu kısım, ağ içindeki bir cihazı benzersiz bir şekilde tanımlar. Bu, telefon numarasının son rakamları gibi, belirli bir ağ içindeki bir cihazı belirlemek için kullanılır.

Alt ağ maskesi (subnet mask), IP adresinin hangi bölümünün "network" kısmı, hangisinin "host" kısmı olduğunu belirler. Örneğin, 255.255.255.0 alt ağ maskesi, ilk 3 byte'ın "network" kısmını belirler, geriye kalan son byte'ın ise "host" kısmını. Yani, alt ağ maskesi, IP adresinin hangi kısmının ağ bilgisini, hangi kısmının ise cihazın benzersiz kimliğini temsil ettiğini gösterir.

### IPv4'ün Özellikleri
* 32 Bitlik IP Adresi: IPv4, 32 bit uzunluğunda IP adresleri kullanır. Bu, teorik olarak yaklaşık 4.3 milyar benzersiz IP adresi sağlar.
 
* Sayısal ve Noktayla Ayrılmış Adres: IPv4 adresleri, sayısal bir formatta yazılır ve bitleri bir nokta ile ayrılmıştır. Örneğin, 192.168.1.1.
  
* 12 Başlık Alanı ve 20 Byte Uzunluğu: IPv4 başlığı 12 adet alan içerir ve toplam uzunluğu 20 bytedir. Başlık, paketin yönlendirilmesi ve hedefe ulaştırılması için gerekli bilgileri içerir.
  
* Tek, Yayın ve Çok Noktaya Yayın Adresleri: IPv4, tek noktaya yayın, yayın ve çok noktaya yayın tarzında adreslere sahiptir. Bu, özellikle ağ iletişiminde belirli amaçlar için kullanılır.
  
* VLSM (Sanal Uzunluk Alt Ağ Maskesi) Desteği: IPv4, VLSM'yi destekler. Bu, farklı alt ağların farklı uzunluklarda alt ağ maskeleri kullanmasını sağlar.

* Posta Adresi Çözümleme Protokolü (ARP): ARP, IPv4'ün MAC adresini IP adresi ile eşleştirmek için kullanılan bir protokoldür. Bu, veri iletimi sırasında ağdaki cihazların birbirini tanımasını sağlar.

* RIP Protokolü Desteği: RIP (Routing Information Protocol), IPv4 ağlarda kullanılan bir yönlendirme protokolüdür. RIP, yönlendirilen arka plan programları tarafından desteklenir.
  
* Manuel veya DHCP ile Ağ Tasarımı: IPv4 ağları, IP adreslerinin elle atanması veya DHCP (Dynamic Host Configuration Protocol) kullanılarak otomatik olarak dağıtılması gibi yöntemlerle tasarlanabilir.
  
* Paket Parçalanması: IPv4, paketlerin yönlendiricilerden ve ana bilgisayarlardan parçalanmasına izin verir. Bu, farklı ağlarda farklı iletim kontrol protokollerini kullanabilmesini sağlar.

### Adres Çözümleme Protokolü (ARP) Nasıl Çalışır?
Çoğu bilgisayar programı, iletişim kurmak veya bilgi alışverişi yapmak için mantıksal adresler olarak bilinen IP adreslerini kullanır. Ancak, gerçek iletişim OSI modelinin ikinci katmanındaki Fiziksel Adresler (MAC Adresi) üzerinden gerçekleşir. Bu nedenle, cihazların birbirleriyle etkileşimde bulunabilmesi için hedef MAC adresini almak önemlidir.

Bu noktada devreye ARP (Address Resolution Protocol) girer. ARP'nin temel işlevi, IP adreslerini Fiziksel Adreslere çevirmektir. Yani, bir cihaz diğer bir cihazla iletişim kurmak istediğinde, ARP protokolü, hedef cihazın IP adresini alır ve bu IP adresini karşılık gelen Fiziksel Adres (MAC adresi) ile eşleştirir.


IPv4 paketine göz atalım:

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/b71354c1-cf45-4c69-924f-a89310d1fa88)

SÜRÜM: IP protokolünün sürümü (4 bit), IPv4 için 4'tür. 

HLEN: IP başlık uzunluğu (4 bit), başlıktaki 32 bitlik kelimelerin sayısıdır. Bu alanın minimum değeri 5, maksimum değeri 15'tir. 

Hizmet türü: Düşük Gecikme, Yüksek Verim, Güvenilirlik (8 bit) 

Toplam Uzunluk: Minimum değeri 20 bayt ve maksimum değeri 65.535 bayt olan başlık + Veri (16 bit) uzunluğu. 

Tanımlama: Tek bir IP datagramının (16 bit) parça grubunu tanımlamak için Benzersiz Paket Kimliği 

Bayraklar: Her biri 1 bitlik 3 bayrak: ayrılmış bit (sıfır olmalıdır), parçalanma bayrağı, daha fazla parça bayrağı (aynı sıra) 

Parça Ofseti: Belirli Datagramdaki belirli parçanın önündeki Veri Baytlarının sayısını temsil eder. Maksimum değeri 65.528 bayt olan 8 bayt sayısı cinsinden belirtilir. 

Yaşam Süresi: Datagram'ın ömrü (8 bit), Bir Paketin Hedefe teslim edilmeden önce aldığı Hop sayısını kısıtlayarak datagramın ağ üzerinden döngü yapmasını engeller.

Protokol: Verinin aktarılacağı protokolün adı (8 bit) 

Başlık Sağlama Toplamı: Datagram başlığındaki hataları kontrol etmek için 16 bitlik başlık sağlama toplamı 

Kaynak IP adresi: Gönderenin 32 bit IP adresi 

Hedef IP adresi: Alıcının 32 bit IP adresi 

Seçenek: Kaynak rotası, kayıt rotası gibi isteğe bağlı bilgiler. Ağ yöneticisi tarafından bir yolun çalışıp çalışmadığını kontrol etmek için kullanılır.

***
Protocol: Burada IP'nin yanı sıra hangi protokolü kullandığımızı bulacaksınız. Hangi aktarım katmanı protokolünü kullandığımızı bu şekilde belirleriz. Yani burada TCP, UDP veya belki başka bir şey bulacaksınız.
Source Address: Burada bu IP paketini oluşturan cihazın IP adresini bulunur.
Destination Address: IP paketini alması gereken cihazın IP adresidir.
***

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

