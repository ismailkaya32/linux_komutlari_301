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

---

<div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/ecc61e7f-7c27-4f56-b492-e382ac812e9a"/>
</div>

- ---

### ps komutu: 

<div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/c8e07aa1-122e-413a-b23e-b0cfea870cab"/>
 </div>

Örnek: ps -ef komuyu ile hangi komutun (sürecin) çalıştığını görme

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/53cefe7d-13a6-432e-bca7-5a203e0ce170"/>
 </div>
 
- ---

Örnek: Sadece ismailkaya'ya ait süreçleri ekrana getirme

- a kelimesi --> Tüm processleri (süreci) listelesin
- u kelimesi --> Vereceğimiz user (kullanıcı) hakkında bilgileri getirme

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/975baa43-592c-4139-af18-0e71b5b73700"/>
 </div>

- ---

Örnek: Sadece root'a ait süreçleri ekrana getirme

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

- htop nasıl indirilir?
 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/539103d2-77d8-47c7-aa97-36f6c3939a2c"/>
 </div>

- ---

### kill komıutu nedir?

- Süreçleri sonlandırmamızı sağlar.
- Bir süreci sonlandırmak için kill komutundan sonra istediğimiz uygulamayı kapatmak için istediğimiz uygulamanın PID kodunu yazıyoruz.

Örnek: gedit uygulamasını sonlandırma

- Sol tarafta gedit uygulamasının çalıştğını görüyoruz.
 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/6bc5151a-b837-4bf4-a20d-9f9cde35c20eb"/>
 </div>

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

Örnek: Terminalden firefox uygulamasını arka planda çalıştırabiliyoruz. Ama terminalde işlem yapamıyoruz.

  <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/cf7a0ffa-0fc6-43d2-bae9-75fe083ea8a9"/>
 </div>
- ---

### nohup ve & kullanımı:

- nohup ve & komutları ile bir uygulamayı hem arka planda çalıştırır hem de terminalde rahatça gezebiliriz.

Örnek: Terminalden firefox uygulamasını hem arka planda çalıştırıp hem de terminalde rahatça hareket edebiliyoruz.

   <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/67186389-9b02-45eb-a794-eb79569b1f3d"/>
 </div>
 
- ---

### ctrl+z ve bg kullanımı:

- Terminalden gedit uygulamasını açtıktan sonra terminalde ctrl+z komutu ile terminalden gedit uygulamasını kapattığımız zaman arka planda gedit uygulaması çalışmıyor. Bundan dolayı gedit uygulamasının çalışması için bg komutunu kullanıyoruz.

1) Terminalden gedit uygulamasının ctrl+z ile arka planda kapandığını görüyoruz.

 <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/6d21da41-860d-4086-8d12-aa397b45d694"/>
 </div>

2) Terminalden gedit uygulamasının ctrl+z ile arka planda kapandığını görüyorduk. Bundan sonra bg komutunu uyguluyoruz. Ve artık hem terminali rahatça kullanabiliyoruz hem de gedit uygulaması arka planda çalıştırabiliyoruz.
   
  <div align="center">
	<img src="https://github.com/ismailkaya32/linux_komutlari_301/assets/122615472/ac9db0de-5bc2-4231-891e-312cdd6cdaf9"/>
 </div>




 
