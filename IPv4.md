### IPv4 Nedir
IP, İnternet Protokolü'nü temsil eder ve IPv4, Sürüm Dört anlamına gelir. Bir IPv4 adresi 32 bittir ve network ve host kısmı olmak üzere 2 bölümden oluşur.

### IPv4 Yapısı
IP adresi, iki temel bileşen içerir: network (ağ) kısmı ve host (ana bilgisayar) kısmından oluşur. Network kısmı, IP adresinin hangi ağa ait olduğunu belirtir ve bu, telefon numarasının şehir veya alan koduna benzetilebilir. Host kısmı ise ağdaki cihazı benzersiz bir şekilde tanımlar, bu da telefon numarasının son rakamlarına benzetilebilir.

### Alt Ağ Maskesi(Subnet Mask)
Örneğin, yerel ağlarda yaygın olarak kullanılan 192.168.1.1 IP adresi, 255.255.255.0 alt ağ maskesiyle birlikte gelir.

Bu IP adresinin ilk 3 byte'ı (24 bit) "network" kısmını temsil eder. Bu kısım, cihazın hangi ağa ait olduğunu belirtir ve genellikle tüm cihazlar aynı ağ içerisinde bulunur. Bu benzetmeye telefon numarası örneğinden devam edecek olursak, ilk 3 byte, bir şehir veya bölge kodunu temsil eder.

Son byte (8 bit), ise "host" kısmını temsil eder. Bu kısım, ağ içindeki bir cihazı benzersiz bir şekilde tanımlar. Bu, telefon numarasının son rakamları gibi, belirli bir ağ içindeki bir cihazı belirlemek için kullanılır.

Alt ağ maskesi (subnet mask), IP adresinin hangi bölümünün "network" kısmı, hangisinin "host" kısmı olduğunu belirler. Örneğin, 255.255.255.0 alt ağ maskesi, ilk 3 byte'ın "network" kısmını belirler, geriye kalan son byte'ın ise "host" kısmını. Yani, alt ağ maskesi, IP adresinin hangi kısmının ağ bilgisini, hangi kısmının ise cihazın benzersiz kimliğini temsil ettiğini gösterir.

### IPv4'ün Özellikleri
* 32 Bitlik IP Adresi: IPv4, 32 bit uzunluğunda IP adresleri kullanır. Bu, teorik olarak yaklaşık 4.3 milyar benzersiz IP adresi sağlar.
 
* Sayısal ve Noktayla Ayrılmış Adres: IPv4 adresleri, sayısal bir formatta yazılır ve bitleri bir nokta ile ayrılmıştır. Örneğin, 192.168.1.1.
  
* Tek, Yayın ve Çok Noktaya Yayın Adresleri: IPv4, tek noktaya yayın, yayın ve çok noktaya yayın tarzında adreslere sahiptir. Bu, özellikle ağ iletişiminde belirli amaçlar için kullanılır.
  
* VLSM (Sanal Uzunluk Alt Ağ Maskesi) Desteği: IPv4, VLSM'yi destekler. Bu, farklı alt ağların farklı uzunluklarda alt ağ maskeleri kullanmasını sağlar.

* Adresi Çözümleme Protokolü (ARP): ARP, IPv4'ün MAC adresini IP adresi ile eşleştirmek için kullanılan bir protokoldür. Bu, veri iletimi sırasında ağdaki cihazların birbirini tanımasını sağlar.

* RIP Protokolü Desteği: RIP (Routing Information Protocol), IPv4 ağlarda kullanılan bir yönlendirme protokolüdür. RIP, yönlendirilen arka plan programları tarafından desteklenir.
  
* Manuel veya DHCP ile Ağ Tasarımı: IPv4 ağları, IP adreslerinin elle atanması veya DHCP (Dynamic Host Configuration Protocol) kullanılarak otomatik olarak dağıtılması gibi yöntemlerle tasarlanabilir.
  
* Paket Parçalanması: IPv4, paketlerin yönlendiricilerden ve ana bilgisayarlardan parçalanmasına izin verir. Bu, farklı ağlarda farklı iletim kontrol protokollerini kullanabilmesini sağlar.

### Adres Çözümleme Protokolü (ARP)
Çoğu bilgisayar programı, iletişim kurmak veya bilgi alışverişi yapmak için mantıksal adresler olarak bilinen IP adreslerini kullanır. Ancak, gerçek iletişim OSI modelinin ikinci katmanındaki Fiziksel Adresler (MAC Adresi) üzerinden gerçekleşir. Bu nedenle, cihazların birbirleriyle etkileşimde bulunabilmesi için hedef MAC adresini almak önemlidir.

Bu noktada devreye ARP (Address Resolution Protocol) girer. ARP'nin temel işlevi, IP adreslerini Fiziksel Adreslere çevirmektir. Yani, bir cihaz diğer bir cihazla iletişim kurmak istediğinde, ARP protokolü, hedef cihazın IP adresini alır ve bu IP adresini karşılık gelen Fiziksel Adres (MAC adresi) ile eşleştirir.

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/4ea9fe2b-3cd5-42bf-98a2-585cd03d79e7)

### ARP Türleri

#### Proxy ARP:
Tanım: Proxy ARP, ağdaki bir cihazın başka bir cihaza yönelik ARP isteklerini yanıtladığı bir tekniktir. Bir yönlendiricinin, aynı alt ağda olmayan cihazlar adına ARP isteklerine yanıt vermesini sağlar.
Kullanım Durumu: Proxy ARP, farklı alt ağlardaki cihazların iletişim kurması gereken senaryolarda yaygın olarak kullanılır ve Proxy ARP'nin etkin olduğu bir yönlendirici, trafiğin iletilmesine yardımcı olur.

#### Gratuitous ARP:
Tanım: Karşılıksız ARP, kaynak ve hedef IP adreslerinin gönderenin IP adresine ayarlandığı bir ARP isteği veya yanıt paketidir. Ağdaki diğer cihazların ARP önbelleklerini gönderenin MAC adresiyle ilgili yeni bilgilerle güncellemek için kullanılır.
Kullanım Örneği: Karşılıksız ARP genellikle bir cihaz MAC adresinde veya IP adresinde bir değişiklik duyurmak istediğinde kullanılır ve diğer cihazların ARP önbelleklerini güncellemesine yardımcı olur.

#### Reverse ARP (RARP):
Bir cihazın yalnızca MAC adresini bildiği halde IP adresini keşfetmek için kullandığı bir protokoldür. Ağa MAC adresini içeren bir yayın isteği göndererek çalışır ve RARP sunucusu karşılık gelen IP adresiyle yanıt verir.
Kullanım Örneği: RARP günümüzde daha az yaygındır ancak geçmişte özellikle disksiz iş istasyonlarında önyükleme sırasında bir IP adresi elde etmek için kullanılmıştır

#### Inverse ARP (InARP):
Çerçeve Rölesi ve Asenkron Aktarım Modu (ATM) ağlarında, bilinen veri bağlantısı katmanı adresine dayalı olarak bir PVC'nin (Kalıcı Sanal Devre) diğer ucunun IP adresini keşfetmek için kullanılır.
Kullanım Durumu: InARP, özellikle cihazların, Çerçeve Aktarmadaki belirli bir Veri Bağlantısı Bağlantı Tanımlayıcısı (DLCI) veya ATM ağlarındaki Sanal Yol Tanımlayıcısı/Sanal Kanal Tanımlayıcısı (VPI/VCI) ile ilişkili IP adresini öğrenmesi gereken durumlarda geçerlidir.

### ARP Nasıl Çalışır
1.  Başlatma( Initialization):
Bir cihaz bir ağa bağlandığında genellikle boş bir ARP önbelleğiyle başlar. ARP önbelleği, IP adresleri ve karşılık gelen MAC adresleri arasındaki eşlemeleri saklayan bir tablodur.

2. Adres Çözümleme İhtiyacı:
Bir cihaz aynı ağdaki başka bir cihazla iletişim kurmak istediğinde hedef cihazın MAC adresini bilmesi gerekir. Cihazın ARP önbelleğinde MAC adresi yoksa adresi çözümlemek için ARP gerçekleştirmesi gerekir.

3. ARP İsteği (ARP Request):
Gönderen cihaz yerel ağa bir ARP İsteği mesajı yayınlar. Bu ARP İsteği, gönderenin MAC ve IP adreslerini ve MAC adresini bulmaya çalıştığı hedef IP adresini içerir.Yayın, gönderen cihazın hedefin MAC adresini bilmemesi ve yerel ağdaki tüm cihazların isteği duymasını istemesi nedeniyle gereklidir.

4. ARP İsteğinin Alınması:
Ağdaki tüm cihazlar ARP İsteğini alır ancak yalnızca eşleşen IP adresine sahip cihaz yanıt verir.

5. ARP'nin Cevabı (ARP Reply):
Eşleşen IP adresine sahip cihaz, istekte bulunan kişiye doğrudan bir ARP Yanıtı gönderir. ARP Yanıtı gönderenin MAC adresini içerir.Orijinal istek sahibi, ARP önbelleğini alınan bilgilerle günceller.

6. ARP Önbelleğe Alma (ARP Caching):
Hem istekte bulunan hem de yanıtlayan, ARP önbelleklerini IP-MAC adres eşlemesiyle günceller. Cihazlar artık ARP sürecinden geçmeden doğrudan birbirlerine adreslenebildiğinden, bu gelecekteki iletişimlerde yardımcı olur.

7. İletişim:
ARP önbelleği güncellendiğinde cihazlar artık doğrudan MAC adreslerini kullanarak iletişim kurabilir. Bu cihazlar arasındaki sonraki iletişim, ARP önbellek girişinin süresi dolana veya açıkça temizlenene kadar ARP gerektirmez.

8. ARP Önbellek Yaşlandırma (ARP Cache Aging):
ARP önbelleklerinin zaman aşımı vardır ve girişler belirli bir süre sonra sona erer. Bu, cihazların yeni IP adresleri alması veya değiştirilmesi gibi ağdaki değişikliklere uyum sağlamaya yardımcı olur.


IPv4 paketine göz atalım:

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/b71354c1-cf45-4c69-924f-a89310d1fa88)

* Version (4 bits): IP sürümünü belirtir ve IPv4 için bu alan "4" olarak ayarlanmıştır.
  
* Header Length (IHL - 4 bits): IPv4 başlığının uzunluğunu 32 bitlik sözcüklerle temsil eder. Minimum değer 5 ve maksimum 15'tir.
  
* Type of Service (TOS) or Differentiated Services Code Point (DSCP) - 8 bits: Başlangıçta hizmet kalitesini belirlemek için tasarlanmış olup, modern ağlarda DSCP olarak yeniden tanımlanarak hizmet sınıflarının daha ayrıntılı bir tanımına olanak sağlanmıştır.

* Total Length (16 bits): IPv4 paketinin (başlık + veri) toplam uzunluğunu bayt cinsinden belirtir.
  
* Identification (16 bits): Tek bir IP datagramının bir grup parçasını benzersiz şekilde tanımlamak için kullanılır.
  
* Flags (3 bits): "Parçalama" (DF) bayrağını, "Daha Fazla Parça" (MF) bayrağını ve bir ayrılmış biti içerir.

* Fragment Offset (13 bits): Orijinal parçalanmamış IP datagramının başlangıcına göre belirli bir parçanın uzaklığını gösterir.

* Time to Live (TTL - 8 bits): Bir paketin atılmadan önce alabileceği maksimum atlama sayısını temsil eder.
  
* Protocol (8 bit): IP datagramının veri bölümünde kullanılan protokolü tanımlar. Örneğin TCP, UDP, ICMP.

* Header Checksum (16 bits): Başlığın hata kontrolü için kullanılır. Sağlama toplamı veriler hariç yalnızca başlık üzerinden hesaplanır.

* Source Address (32 bits): Paketin kaynak IP adresini belirtir.
* Destination Address (32 bits): Paketin hedef IP adresini belirtir.
* Options (Variable): Kayıt rotası, zaman damgası ve diğerleri gibi çeşitli seçenekleri içerebilen isteğe bağlı bir alan.
  
* Padding: Gerekirse başlık uzunluğunun 32 bitin katı olmasını sağlamak için dolgu eklenir.






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

