# React Native Tabanlı Kampüste Akşam Pazarı(KAP) Mobil Uygulaması

Kampüste Akşam Pazarı mobil uygulaması, bir sosyal sorumluluk 
projesi hedefiyle, üniversite öğrencilerine yönelik; ürün ve hizmetlerin sunulmasını 
sağlayan bir mobil uygulama girişimidir. Bu uygulama sayesinde öğrenciler ücretsiz veya 
uygun fiyatlarla arzu ettikleri ürünlere ulaşabileceklerdir. Kampüs içinde bulunan gıda 
işletmecileri, yemek hizmeti veren yerler, marketler vb. işletmecilerin ellerinde bulunan, 
satılamayan ve çöpe gidecek ürünlerin tazeliği bozulmadan uygun veya ücretsiz bir 
şekilde bir “akşam pazarı” sloganıyla öğrencilere, tüketicilere ulaştırılması, pazarlanması 
hedef alınmaktadır. Böylece hem gıda israfı önlenmiş olacak hem de ihtiyaç sahibi 
öğrenciler bu uygulamadan, girişimden faydalanabileceklerdir.

KAP mobil uygulamasının temel amacı; bir öğrencinin en temel gereksinimi olan 
beslenme, beslenebilme ihtiyacını hedef almaktadır. Bu hedef doğrultusunda, yiyecek 
içecek hizmeti sunan işletmelerin ürettikleri yiyecekleri, satışa sunduğu gıdaları, gün 
sonunda ya da müşteri olmayan durgun saatlerde, uygulama üzerinden ilana çıkararak 
satmaları amaçlanmaktadır. Böylece hem fazla olan gıdaları çöpe dökmemiş olacaklar 
hem de yenilebilir durumda olan gıdalar daha uygun fiyatlardan tüketici ile buluşmuş 
olacaktır.

Bunun yanında işletmeler sosyal sorumluluk davranışı olarak, artan gıdaları yine 
uygulama üzerinden ücretsiz olarak ilana koyabilme hakkına sahiptirler. Çünkü; gün 
içinde halihazırda mevcut kar marjını yakalayan bir işletme fazladan kalan gıdaları 
ihtiyaç sahiplerine uygulama aracılığıyla ulaştırarak sosyal sorumluluk davranışını yerine 
getirebilmektedir.

Daha ayrıntılı inceleyecek olursak; uygulamada yemekler neredeyse %50 
indirimli satılmaktadır. Çünkü; kuruluş amacı ve uygulamanın fikri bu doğrultudadır. 
Türkiye’de yemeksepeti.com dahil birçok yemek satan web sitesi mevcuttur. Fakat KAP 
uygulamasının farkı, hijyenik açıdan tüketilebilecek durumda olan gıdaların tamamını 
satamayan işletmelerin, zaten müşteri olmayan saatlerinde indirime çıkararak, %50 
oranında indirimli fiyatlardan satılmasını sağlamaktır. KAP uygulamasına üye olan 
yiyecek içecek işletmeleri tamamen kontrol altında olacak, hijyen ve sanitasyon 
kurallarına uygun gıdaları uygulamada satabileceklerdir. Aksi durumların önüne 
geçebilmek adına üyelik sözleşmelerinde bunlar detaylı olarak belirtilecek ve bu 
doğrultuda uygulamada her şey açık şekilde belirtilecektir.


## **Platform ve Ortam Kurulumu**
Kampüste Akşam Pazarı (KAP) Uygulaması, React Native çerçevesi kullanılarak ve Javascript dili tercih edilerek Visual Studio Code ortamında geliştirilmiştir. Javascript ve React Native için kullanışlı eklentiler içermesi, Android emulatorle uyumlu çalışmasından dolayı bu IDE tercih edilmiştir. Android Studio'nun sunmuş olduğu emülatörden yararlanılmıştır. Android ve İOS platformlarıyla uyumlu bir 
mobil uygulamadır.

Expo CLI altyapısının özelliklerinden yararlanabilmek için NPM kullanılmıştır. NPM, Node.js'in paket yöneticisidir. Binlerce hazır paket içerir ve bu paketlerin kolayca indirilmesini, 
dosyalara dahil edilmesini sağlar. Bu sayede geliştirme süreci hızlanır ve kolaylaşır. 

Uygulama geliştirilirken Google tarafından sağlanan bulut bilişim hizmeti olan Firebase kullanılmıştır. Uygulama içerisinde kullanıcı kimlik doğrulama ve veri tabanı özellikleri kullanılmıştır.

## Proje Tasarımı

Uygulama içerisinde giriş ekranı, kayıt ekranı, karşılama ekranı ve indirimli 
ürünlerin olduğu anasayfa ekranı bulunmaktadır. Kullanıcıya ait giriş ve kayıt bilgilerini
tutmak için “Firebase” veri tabanı kullanılmıştır. Ayrıca satıcıların indirimli ürün ve ürün 
bilgileri, Firebase veri tabanı üzerinden güncel olarak girilmektedir. İndirimli 
ürünlerde geçerli olan indirim süresini hesaplamak için ise geri sayım bileşeni kullanılmıştır. 


### Uygulama Giriş Ekranı
Kullanıcı uygulamaya girdiğinde ilk olarak giriş ekranıyla karşılaşmaktadır. 
E-posta ve şifre ile giriş yapılmaktadır. Kullanıcı daha önce kayıt oluşturmadıysa 
“Hesabınız yok mu? Üye ol” seçeneğine tıklayarak kayıt oluşturması gerekmektedir. 
Kullanıcı kaydolduktan sonra giriş yapabilmektedir. Giriş yapıldıktan sonra karşılama 
ekranı açılır. 

<p><img align="center" width="350" height="750" src="https://github.com/hafideveloper/React-Native-Mobile-Application/assets/101593285/9c227c95-5870-4e3a-9387-cfdc8101c1bc"/></p>


### Uygulama Kayıt Ekranı
Kullanıcının giriş yapabilmesi için kayıt olması gerekmektedir. Kullanıcıdan ad, 
soyad, email ve şifre istenmektedir. Sonrasında “Kayıt Ol” butonu tıklanarak kayıt 
tamamlanmaktadır. Bu işlem sonrasında kullanıcı giriş ekranına yönlendirilir. Kayıt 
aşamasında kullanılan email ve şifre ile giriş yapılabilmektedir. Kayıt oluşturan 
kullanıcıların bazı bilgileri; adı, soyadı ve eposta adresi veri tabanında tutulmaktadır.

<p><img align="center" width="350" height="750" src="https://github.com/hafideveloper/React-Native-Mobile-Application/assets/101593285/f215d871-f322-4bf9-a129-108189187f7f"/></p>


### Uygulama Karşılama Ekranı
Kullanıcı giriş yaptıktan sonra açılan ekrandır. Karşılama ekranında kullanıcı adı 
belirtilir ve bu bilgi veri tabanından çekilmektedir. İleri butonu bulunmaktadır, bu buton 
tıklandığında indirimli ürünlerin bulunduğu sayfa açılmaktadır. Sade bir karşılama ekranı 
tasarlanmıştır.


<p><img align="center" width="350" height="750" src="https://github.com/hafideveloper/React-Native-Mobile-Application/assets/101593285/397c3f01-fcfb-45c6-afea-9ea3f3fb060e"/></p>


### İndirimli Menü Ekranı

İndirimli ürünlerin bulunduğu ekrandır. Ürün bilgileri, ürünün adı, ürünün 
satıldığı restoran, ürünün fotoğrafı, fiyatı, kalan ürün adedi ve ürünlere uygulanan indirim 
süreleri belirtilmiştir. Bir sayaç kullanılarak her bir ürünün, kalan indirim süresi 
hesaplanmaktadır. Ürünler listeli bir şekilde kullanıcıya sunulmaktadır. 


<p><img align="center" width="350" height="750" src="https://github.com/hafideveloper/React-Native-Mobile-Application/assets/101593285/a2fa9b43-107b-4c91-8f4b-7d98c6eac64c"/></p>

Ürünlerin kalan indirim sürelerini hesaplamak için, veri tabanına girilen indirimin sona ereceği süreden, şimdiki zamanı
çıkararak kalan süre hesaplanır.

#### Ürün Bilgilerinin Veri Tabanında Oluşturulması ve Gösterimi; 

<p><img align="center" width="900" height="350" src="https://github.com/hafideveloper/React-Native-Mobile-Application/assets/101593285/b2d4ce02-5bcd-43e5-aed5-874643b0dccc"/></p>

#### Kullanıcı Kayıt ve Giriş İşlemlerinin Veri Tabanında Tutulması;

<p><img align="center" width="720" height="300" src="https://github.com/hafideveloper/React-Native-Mobile-Application/assets/101593285/387c4a2c-ef8f-4f87-a097-3a0a613fde32"/></p>

#### Bazı Kullanıcı Bilgilerinin Veri Tabanında Tutulması;

<p><img align="center" width="650" height="300" src="https://github.com/hafideveloper/React-Native-Mobile-Application/assets/101593285/da1c77a8-f1f8-4dbd-92b2-06560b6ac45e"/></p>

## Sonuçlar ve Öneriler

Kampüste Akşam Pazarı uygulaması olan KAP, kullanıcılara basit ve anlaşılabilir 
bir arayüz sunarak istedikleri ürünlere vaktinde ve zamanında ulaşabileceği indirimli 
ürünlerin bildirimlerini alabileceği, Kampüs içerisindeki işletmecilerin ellerinde kalan 
ürünleri güvenli ve sağlıklı bir şekilde öğrencilere ulaştırabileceği ve en önemlisi gıda 
israfının önüne geçerek bir sosyal sorumluluk bilinciyle oluşturulan bir uygulama olarak 
hedeflenmiştir. Ayrıca kullanılan teknolojiyle, bu projede iki farklı mobil platform 
kullanıcısına yani üreticilere ve tüketicilere ulaşmak amaçlanmıştır.
Projenin devamında alışveriş ve indirim kampanyaları dışında, kampüs içerisinde 
öğrencilerin birbirleriyle iletişim kurmalarını sağlayan bir ağ, arayüz geliştirilecektir. Bu 
sayede öğrencilerin; birbirleriyle iletişim kurabileceği, yardımlaşabileceği, not paylaşımı, 
kitap-defter gibi kullanmadıkları kırtasiye ürünlerini, ihtiyaç dışı malzemelerini 
birbirleriyle paylaşabileceği, takas yapabileceği veya satışını gerçekleştirebilecekleri bir 
uygulama hedeflenmektedir.
