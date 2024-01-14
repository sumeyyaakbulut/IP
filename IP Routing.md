# IP Routing
İlk olarak, uygulamaların DNS adlarını kullanıyorlarsa DNS adlarını çözümlemesi, bunları bir IP adresine çevirmesi ve kullanılacak aktarım protokolünü kullanacağını seçer. Bu örnekte UDP kullanıyoruz. Bilgi katmanlı modelden aşağıya doğru ağ katmanına ilerledikçe, bir sonraki soru şu oluyor: Hedef nerede, yerel mi yoksa uzak mı?

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/3141fe97-f6e7-4fbf-84d1-a0c1aa44eab3)

* APP DATA: 192.168.4.1'ye göndereceğim bazı veriler var ve güvenilir bir bağlantıya ihtiyacım yoktur. O yüzden UDP kullanacağım. Bana verileri gönderebilirsin.

* Her katmanda, 3.katmana ulaşana kadar başlıklar eklenenecektir. Onu IP başlığına yerleştirecek ve ardından katman 2'den gerçekten bir paket göndermesini isteyecektir.

![image](https://github.com/sumeyyaakbulut/IP/assets/62395974/d314719f-669a-4797-8654-91bcf730cd54)


* Bir UDP başlığı koyacağım.Destination IP eklenir. Destination IP(hedef IP) adresini temsil eder. Bu terim, bir ağ iletişiminde bir paketin hedef IP adresini ifade eder. Destination IP
192.168.4.1 dir. Source IP eklenir. Destination IP adresi, geldiği donanımın IP adresini içeren IP paket alanıdır. Source IP 192.168.5.1 dir.

* Katman 2, “Bu IP hakkında bilgim yok, MAC adresim yok ve bu yüzden bir ARP isteği yoluyla çözmeye çalışacağım” diyerek yanıt verir. Paket park edilecek ve ARP isteği tamamlanana kadar arabelleklerde kalacaktır.

* Bu noktada, tam 3. ve 2. katman arasında cihaz şunu söyleyecektir: “Peki, bu IP adresine ve bu maskeye göre burada /24 var. Hedef farklı bir ağda bulunmaktadır. 192.168.5 ağındayım ve hedef 192.168.4 ağındadır."
