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

