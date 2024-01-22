# IP Routing
İlk olarak, uygulamaların DNS adlarını kullanıyorlarsa DNS adlarını çözümlemesi, bunları bir IP adresine çevirmesi ve kullanılacak aktarım protokolünü kullanacağını seçer. Bu örnekte UDP kullanıyoruz. Bilgi katmanlı modelden aşağıya doğru ağ katmanına ilerledikçe, bir sonraki soru şu oluyor: Hedef nerede, yerel mi yoksa uzak mı?

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/3141fe97-f6e7-4fbf-84d1-a0c1aa44eab3)

APP DATA: 192.168.4.1'ye göndereceğim bazı veriler var ve güvenilir bir bağlantıya ihtiyacım yoktur. O yüzden UDP kullanacağım. Bana verileri gönderebilirsin.

Her katmanda, 3.katmana ulaşana kadar başlıklar eklenenecektir. Onu IP başlığına yerleştirecek ve ardından katman 2'den gerçekten bir paket göndermesini isteyecektir.

 ![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/d314719f-669a-4797-8654-91bcf730cd54)


Bir UDP başlığı koyacağım. Destination IP eklenir. Destination IP(hedef IP) adresini temsil eder. Bu terim, bir ağ iletişiminde bir paketin hedef IP adresini ifade eder. Destination IP 192.168.4.1 dir. Source IP eklenir. Destination IP adresi, geldiği donanımın IP adresini içeren IP paket alanıdır. Source IP 192.168.5.1 dir.

Katman 2, bu IP hakkında bilgim yok, MAC adresim yok ve bu yüzden bir ARP isteği yoluyla çözmeye çalışacağım” diyerek yanıt verir. Paket park edilecek ve ARP isteği tamamlanana kadar arabelleklerde kalacaktır.

Bu noktada, tam 3. ve 2. katman arasında cihaz şunu söyleyecektir: Peki, bu IP adresine ve bu maskeye göre burada /24 var. Hedef farklı bir ağda bulunmaktadır. 192.168.5 ağındayım ve hedef 192.168.4 ağındadır.

Bunun nedeni yine ağ tanımlayıcısının IP adresinin ilk 3 byte bulunduğunu belirten alt ağ maskesidir. Yani ARP süreci şöyle diyor: "Ama onları hedeflenen hedefin MAC adresi için çözmeme gerek yok. Yönlendirici değilim ve bunu nasıl göndereceğimi bilmiyorum, ancak varsayılan ağ geçidim bunu bilecek, bu nedenle cihazın IP protokolü yapılandırmasında yapılandırılmış olan varsayılan ağ geçidinin MAC adresini çözmeye çalışacağım.

Bu muhtemelen hataların ve hataların ilk ve en yaygın kaynaklarından biridir ve bu sorunu giderirken doğru varsayılan ağ geçidi IP adresinin yapılandırıldığından emin olmalıyız. Nereye göndereceğimi veya bunu hangi yönlendiricinin işlemesi gerektiğini bilmiyorsam paket oraya ulaşmayacaktır.

 ![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/7022aabc-982d-46ef-bfc7-1427c279dcf6)


DST MAC Broadcast, bir cihazın ağdaki tüm diğer cihazlara ulaşmak için kullandığı bir MAC adresidir. Genellikle "FF:FF:FF:FF:FF:FF" gibi bir yayın MAC adresini temsil eder. Örneğin, bir cihaz ARP Request göndermek istediğinde, bu isteği ağdaki tüm cihazlara yönlendirmek için DST MAC Broadcast kullanılır. SRC MAC, bir veri paketinin kaynak cihazının MAC adresini temsil eder. Bu adres, gönderen cihazın ağdaki benzersiz tanımlayıcısıdır. ARP Request, bir cihazın ağdaki başka bir cihazın IP adresine karşılık gelen MAC adresini öğrenmek için gönderdiği bir ARP paketidir. Bu paket, hedef IP adresini içerir ve ağdaki tüm cihazlara yayınlanır. ARP Request'in amacı, belirli bir IP adresine karşılık gelen MAC adresini bulmak ve ağ cihazları arasında bu çözümlemeyi sağlamaktır.
Proxy ARP, ağdaki bir cihazın, başka bir cihazın IP adresi için MAC adresini sağlama yeteneğidir. Yani, bir cihaz kendi IP adresine sahip olmasa bile, diğer cihazların bu IP adresini çözmelerine yardımcı olabilir.
Özellikle yönlendiriciler, proxy ARP işlevselliğini kullanarak, kendilerine yönlendirilmemiş olan ARP isteklerine yanıt verebilirler. Bu, yönlendiricinin sahip olduğu IP adresleri için diğer cihazların MAC adreslerini sağlamak anlamına gelir.
Bu, varsayılan ağ geçidi (gateway) çağrılarına yanıt verebilmek ve yanlış yapılandırılmış makinelerden gelen bu tür ARP isteklerini ele alabilmek için kullanılır.
Proxy ARP kullanımının kendine özgü güvenlik sonuçları vardır. Özellikle, ağdaki cihazların birbirleriyle doğrudan iletişim kurma yeteneğini artırabilir, ancak aynı zamanda kötü amaçlı kullanımlara açık bir durum yaratabilir.
Yanlış yapılandırılmış veya kötü niyetli bir cihaz, proxy ARP kullanarak ağdaki diğer cihazları yanıltabilir veya saldırabilir.
Bu nedenle, güvenlik politikaları, proxy ARP ve benzeri mekanizmaların nasıl yapılandırılacağına dair dikkatli bir şekilde belirlenmelidir.

 ![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/ca3e3478-e127-4bc1-ac86-9d7ac724939a)

Az önce bir ARP isteği aldığını, 0800:0222:2222 Mac adresiyle ARP tabloma 192.168.5.1 ana bilgisayarını ekleyeyim. Her durumda yönlendirici isteği alacak ve paket iletme işlemini başlatacaktır. İlk önce gönderen makinenin MAC adresini ve IP adresini kendi ARP tablosuna kaydedecektir. Yönlendirici de diğerleri gibi bir IP cihazıdır ve bu nedenle tüm IP kurallarına uyacaktır.

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/a38d3b2a-e705-40a7-8271-ff4fc976849b)

Bu durumda yönlendirici, “Hey, bu benim MAC adresim; paketleri bana iletmeye başlayabilirsin.” Artık gönderen ana bilgisayarın ARP tablosunda ağ geçidi IP adresini ağ geçidi MAC adresine bağlayan bir eşleme vardır. Hedefe iletilmek üzere paketleri bu ağ geçidine göndermeye hazırdır.

Az önce 192.168.5.2'den bir ARP yanıtı aldım. IP'sini ve MAC'ini ARP tabloma ekleyedim. Artık varsayılan ağ geçidim için bir eşlemem var. Katman 2'ye 192.168.4.2 için bir eşleme verebilirim.
Katman 2'ye 192.168.4.2 için bir eşleme  0800:0333:2222 verilir.

Bu girişler eninde sonunda zaman aşımına uğrayacaktır ve bu nedenle boş zamanlara ve mutlak sürelere bağlı olarak ARP işlemi konuşma boyunca tekrarlanabilir.

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/256318eb-1c11-4f5b-9859-4a37f54e4fd1)

Beklemeye alınan paket, amaçlanan hedefin IP adresi, gönderenin kaynak IP adresi, gönderenin kaynak MAC'i ve hedef MAC, yönlendiricinin MAC adresi kullanılarak serbest bırakılır ve gönderilir.

Sadece router'da routing fonksiyonundan bahsettiğimize göre bu cihazın sadece routing fonksiyonu ile nasıl belli bir katmana çıkacağını anlıyoruz. Yönlendirici yalnızca katman 3'te çalışır ve bu nedenle çerçevenin geldiğini görecektir. Onu sindirecek ve işleyecektir, çünkü katman 2'deki MAC adresi açısından kendisine yönlendirilmiştir. Kapsülden arındıracak ve katman 3'e gönderecek ve yönlendirme ve iletme fonksiyonunun gerçekleştiği katman 3'tedir. Bu nedenle hedef IP adresi yönlendiricinin adresi olmasa da yönlendirici, "Ben bir yönlendiriciyim, bu yüzden bunu yönlendirme tabloma göre iletmek istiyorum" diyecektir.

Yönlendirme tablosuna göz atarken yönlendirici, hedef IP'nin o tablodaki bir giriş olduğunu fark edecektir. 192.168.4.0'a uygun maske ile doğrudan bağlı bir segmente bakın; aslında Hızlı Ethernet 0/1'de bulunur. Daha sonra karar, doğrudan katman 2 sürecine göndermek ve katman 2'nin hedefin MAC adresini çözmesini sağlamaktır. Eğer bu doğrudan bağlantılı bir bölüm değilse, yönlendirme tablosundaki giriş, yoldaki başka bir yönlendiricinin IP adresi biçimindeki bir sonraki atlama noktasına işaret edecektir. Bu noktada, yönlendirici bu ara cihaza yönlendirme talebinde bulunacak ve böylece ARP çözümlemesi, kendi MAC adresini bulmak için o cihaza karşı devam edecektir. Buradaki durum, birbirine bağlı iki ağın olduğu basit bir senaryodur.

Bu noktada, yönlendirici bu ara cihaza yönlendirme talebinde bulunacak ve böylece ARP çözümlemesi, kendi MAC adresini bulmak için o cihaza karşı devam edecektir. Buradaki durum, birbirine bağlı iki ağın olduğu basit bir senaryodur.
Bu nedenle, yönlendiricinin ağ katmanı, hedef IP'ler alanına hedef makinenin IP adresi de dahil olmak üzere IP başlığını bir araya getirecektir. Katman 2'de bu bir ara adımdır ve bu nedenle MAC adresi değiştirilir.
ARP isteği." Unutmayın, bu 2. katmandaki bir yayındır ve bu nedenle o segmentteki tüm makineler bunu görecek, işleyecek ve yanıt vermeleri gerekip gerekmediğine karar verecektir.
ARP yanıtı gönderilmeden önce hedef makine, yönlendiricinin IP'sinin eşlemesini ARP tablosundaki MAC adresine de kaydedecektir. Bu nedenle, makinelerin yalnızca bir ARP yanıtı gördüklerinde değil, aynı zamanda bir ARP isteği gördüklerinde de ARP tablosunu nasıl dolduracaklarını görmek ilginçtir. 
