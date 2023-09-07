### **Komutlara giriş 3:**

 ## SÜREÇ(PROCESS) KAVRAMI
  
- Linux'ta çalışan her program bir süreçtir.
- Ancak bir program, birden fazla süreç olarak çalışabilir.
- Zaman kazandırır.
- PID her seferinde değişmektedir.

Bu süreç(process) kavramını daha iyi anlayabilmek için system monitore giriyoruz.
 
<div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/fcf5bfc3-c0f1-414e-bb9e-18ba4c2d9195"/>
</div>

 <br/>

<div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/ecc61e7f-7c27-4f56-b492-e382ac812e9a"/>
</div>

- ---

### ps komutu: 

<div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/c8e07aa1-122e-413a-b23e-b0cfea870cab"/>
 </div>
 <br/>

Örnek: Aşağıdaki örnekte ps -ef komutu ile hangi komutun (sürecin) çalıştığını görüyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/53cefe7d-13a6-432e-bca7-5a203e0ce170"/>
 </div>
 
- ---

Örnek: Aşağıdaki örnekte sadece ismailkaya'ya ait süreçleri ekrana getirme işlemini görüyoruz.

- a kelimesi --> Tüm processleri (süreci) listelesin
- u kelimesi --> Vereceğimiz user (kullanıcı) hakkında bilgileri getirme

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/975baa43-592c-4139-af18-0e71b5b73700"/>
 </div>

- ---

Örnek: Aşağıdaki örnekte sadece root'a ait süreçleri ekrana getirme işlemini görüyoruz.

- a kelimesi --> Tüm processleri (süreci) listelesin
- u kelimesi --> Vereceğimiz user (kullanıcı) hakkında bilgileri getirme

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/0069cb47-b2a3-4c15-9c33-2a8301cc9ac2"/>
 </div>
 
- ---

### htop nedir?

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/cdaf0628-4276-4dca-bd07-e3dc267b63f7"/>
 </div>
 
  <br/>

htop nasıl indirilir?

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/539103d2-77d8-47c7-aa97-36f6c3939a2c"/>
 </div>

<br/>

 <div align="center">
	<img src="https://github.com/ismailkaya32/temel_linux_301/assets/122615472/3be91ebe-4803-4ef2-891b-151dcd29926c"/>
 </div>  

 - Lacivert kutu içine aldığım CPU% kısmı bir uygulamanın ne kadar işlemci harcadığını gösteriyor.
 - Beyaz kutu içine aldığım MEM% kısmı bir uygulamanın ne kadar hafıza (RAM) kullandığını gösteriyor.

<br/>
<br/>

- Klavyeden F5 tuşuna baınca süreçleri ağaç konumuna getiriyor. Aşağıdaki görselde kırmızı ok ile gösterilen yerde mavi mavi dallanmaların olduğunu görebilirsiniz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/temel_linux_301/assets/122615472/ab9e9e70-dd4b-4409-82d1-46672ca6b481"/>
 </div>  


- ---

### kill komutu nedir?

- Süreçleri sonlandırmamızı sağlar.
- Bir süreci sonlandırmak için kill komutundan sonra istediğimiz uygulamayı kapatmak için istediğimiz uygulamanın PID kodunu yazıyoruz.

 <br/>

Örnek: Aşağıdaki örnekte gedit uygulamasını sonlandırma işlemini görüyoruz.

- Sol tarafta gedit uygulamasının çalıştığını görüyoruz.
 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/6bc5151a-b837-4bf4-a20d-9f9cde35c20eb"/>
 </div>
 
 <br/>

- kill 5070(gedit PID kodu) komutunu yazınca gedit uygulamasının kapandığını görüyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/72768691-e61c-49dd-ab25-05acf9330471"/>
 </div>

- ---


!!! Bir uygulamayı sonlandırmak istediğimiz zaman grep komutu ile kısa yoldan o uygulamayı bulmak isteriz. grep komutu ile uygulamanın ismini arattığımızda iki tane satır çıkarsa bunlaradn biri kapatılır. Bunlardan bir tanesi sonlandıracağımız PID'ye sahip iken diğeri sabit PID'ye sahiptir. Genellikle sonlandıracağımız uygulamanın son kısımlarında application yazmaktadır. Ama eğer ikiden fazla satır geliyorsa tüm satırı kapatmamız gerekir.

Örnek: Aşağıdaki örnekte iki satır olan örneğimizi göreceğiz.

- Sol tarafta gedit uygulamasının çalıştğını görüyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/73bff42b-7eed-4d9c-94b1-91040b678763"/>
 </div>

- kill 5687(gedit PID kodu) komutunu yazınca gedit uygulamasının kapandığını görüyoruz.
  
  <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/f661b4ec-a498-4da2-85cc-40546797f6d0"/>
 </div>

 - ---

Örnek: Aşağıdaki örnekte iki satırdan fazla olan örneğimizi görüyoruz.

- Sol tarafta firefox uygulamasının çalıştğını görüyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/f452e229-9711-4b73-b8c7-855a6c4f3425"/>
 </div>

  <br/>

- pkill firefox komutunu yazınca firefox uygulamasının kapandığını görüyoruz. Burada tüm firefox içeren süreci kapatmış oluyoruz. Buradan hem PID kodu bilmeden direkt isimden öldürme işlemini yapabildiğimiz görmüş olduk. Bunu iki satırlı örneklerde de kullanabiliriz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/33f83abc-5640-428e-a0c7-bd46081789f7"/>
 </div>

- ---

### kill -9 ve kill -15 kullanımı:
 
- kill -9 komutu açık olan programı çok hızlı yani ani bir şekilde kapatır. (İstenmeyen veri kaybına sebebiyet verebilir.)
  
 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/32e6968e-122e-41d6-80cf-15a8e3370269"/>
 </div>

- kill -15 komutu açık olan programı normal bir sürede kapatır. (Dosyaları kaydetmeye vakti olduğu için tercih edilebilir.)
  
  <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/772e2ada-8c34-4b8c-afd7-183620c4d2fe"/>
 </div>

- ---

### & kullanımı:

- & komutu ile terminalden arka planda uygulama çalıştırabiliriz. Ama terminalde işlem yapamayız. 

Örnek: Aşağıdaki örnekte terminalden firefox uygulamasını arka planda çalıştırabiliyoruz. Ama terminalde işlem yapamıyoruz.

  <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/cf7a0ffa-0fc6-43d2-bae9-75fe083ea8a9"/>
 </div>
 
- ---

### nohup ve & kullanımı:

- nohup ve & komutları ile bir uygulamayı hem arka planda çalıştırır hem de terminalde rahatça gezebiliriz.

Örnek: Aşağıdaki örnekte terminalden firefox uygulamasını hem arka planda çalıştırıp hem de terminalde rahatça hareket edebiliyoruz.

   <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/67186389-9b02-45eb-a794-eb79569b1f3d"/>
 </div>
 
- ---

### ctrl+z , bg ve disown kullanımı:

- ctrl+z kısayolu, işlemi arka plana almamızı sağlar.
- bg komutu, arka planda çalışan işleri görmemizi sağlar.
- disown komutu, terminali kapattıktan sonra uygulamanın devam etmesini sağlar.

 <br/>

1) Aşağıdaki görselde terminalden ctrl+z komutu ile gedit uygulamasını arka plana alıyoruz. Ama hem gedit uygulaması hata veriyor hem de terminalde işlem yapamıyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/6d21da41-860d-4086-8d12-aa397b45d694"/>
 </div>

 <br/>

2) Az önce hem gedit uygulamasın hata verdiğini hem de terminalde işlem yapamadığımızı görüyorduk. Bundan dolayı sonra `bg` komutunu uyguluyoruz. Ve gedit uygulamasının hata vermesi düzeliyor ama bu sefer yine terminalde hareket edemiyoruz.
   
  <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/ac9db0de-5bc2-4231-891e-312cdd6cdaf9"/>
 </div>

 <br/>

3) Az önce bg komutu ile gedit uygulamasının hata vermesinin düzeldiğini ama bu sefer terminalde hareket edemediğimizi gördük. Bundan dolayı sonra `disown` komutunu kullanıp gedit uygulamasının terminalden bağını kesiyoruz. Ve hem terminalde rahatça hareket edebiliyoruz hem de gedit uygulaması arka planda güzelce çalışıyor. Artık terminali kapatsak dahi gedit uygulaması çalışmaya devam edecek.

<div align="center">
	<img src="https://github.com/ismailkaya32/temel_linux_301/assets/122615472/5202e4f4-d2a5-4969-84a8-43fff53da849"/>
 </div>

<br/>

- Aşağıdaki görselde terminalin kapalı hali ile bile gedit uygulamasının çalıştığını görebiliyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/temel_linux_301/assets/122615472/c3cc2a9c-91e2-4e35-9ca4-4f135d589a67"/>
 </div>   

- ---

### Servis Kavramı: 

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/0b4c6ed5-a411-49ff-8536-c636aaba7c08"/>
 </div>

- ---
 
 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/e3bfe5ba-d5c6-41cb-b012-e89bf3d91292"/>
 </div>

- ---

### systemctl programı:

- Linux'ta sistem üzerindeki servisleri yönetmemizi sağlar.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/1b8afeb1-6ba3-4a94-a27e-ac4432b6e3cb"/>
 </div>

- ---

- `list-units --type service` komutu sistem üzerindeki servis ünitelerini görüntülemizi sağlar.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/cd269ac8-5b0e-4dd1-ad37-b3fbd4995971"/>
 </div>

- ---

- `list-units --type service --state runnig` komutu sistem üzerindeki yalnızca o an çalışan servis ünitelerini görüntülememizi sağlar.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/9fc44a1e-d407-448e-b15a-73f1723164a3"/>
 </div>

<br/>

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/66d0558c-e565-4317-8245-efd4fa975105"/>
 </div>

- ---

- Örnek: Aşağıdaki örnekte bir program veya uygulama hakkında bilgi almak için `systemctl status program_adi` komutunu kullandığımızı görüyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/d719c796-c17a-4837-80fb-a13a66fd217b"/>
 </div>

- ---

Örnek: Aşağıdaki örnekte `sudo systemctl stop uygulama_adi` komutu ile bir uygulamayı veya programı sonlandırabiliyoruz. Ama bu işlemi her daim yönetici olarak yani root olarak yapabiliriz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/472c2fd7-6951-4de5-9951-6ca096770670"/>
 </div>

- ---

Örnek: Aşağıdaki örnekte `sudo systemctl start uygulama_adi` komutu ile bir uygulamayı veya programı başlatabiliyoruz. Ama bu işlemi her daim yönetici olarak yani root olarak yapabiliriz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/46be7c80-6e9b-4e9c-8943-78a5ee49d8e6"/>
 </div>

- ---


Örnek: Aşağıdaki örnekte sudo systemctl restart komutu ile bir uygulamayı veya programı yeniden başlatabiliyoruz. Ama bu işlemi her daim yönetici olarak yani root olarak yapabiliriz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/7c75389d-c26e-496b-b8a2-b47ecee39b3f"/>
 </div>

 
