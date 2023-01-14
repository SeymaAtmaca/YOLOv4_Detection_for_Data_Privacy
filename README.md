# YOLOv4_Detection_for_Data_Privacy

<br><br>
<h1> Türkçe  </h1> 
Bu repo, veri güvenliği için YOLOv4 nesne tespiti ile oluşturulmuş bir projenin dosyalarını içermektedir. <br>

* Program ilk olarak COCO veri seti ile elde edilen YOLOv4 ağırlıklarını indirir ve genel kütüphane kurulumlarını gerçekleştirir.<br> 
* Daha sonra tespit edilen sınıflar arasında "person" var ise veri bölümü aktifleşir ve tespit sırasında işlenen görüntü "Login" dosyası altına kaydedilir. Bu noktada programı test eden kişilerin Google Drive klasörleri altına "Login" klasörü oluşturmaları gerekmektedir <br><br>
* <b>NOT</b> : "person" etiketi, kullanıcıların test edebilmesi için konulmuştur. Bu noktada kendi veri setiniz ile bir tespit modeli eğitimi yaparak programı özelleştirebilirsiniz.<br><br>
* "person" tespitinden sonra kullanıcıdan bir "password " girmesi istenir.  <br>
* Alınan "password" sistemde şifreli olarak saklanan password ile aynı ise kullanıcının yapmak istediği işlem "encode, decode" şeklinde sorulur. <br>
* Encode, kullanıcıdan aldığı veriyi bir "fernet" anahtarı ile şifreleyerek "enc_message_file.csv" dosyasına kaydeder. <br>
* Encode için kullanılan "fernet" anahtarı da "key.csv" içine kaydedilir. Bu anahtar, decode sırasında metni tekrar açabilmek için gerekmektedir. Eğer kullanıcı ilk başta yanlış "password" girmişse sistem sonlanır. <br><br><br>







<h1> English </h1>
This repo contains files of a project created with YOLOv4 object detection for data security. <br>

* The program first downloads the YOLOv4 weights obtained with the COCO dataset and performs the general library installations.<br>
* If there is "person" among the detected classes later, the data section is activated and the image processed during detection is saved under the "Login" file. At this point, people testing the program should create a "Login" folder under their Google Drive folder <br><br>
* <b>NOTE</b> : The "person" tag has been added for users to test. At this point, you can customize the program by training a detection model with your own dataset.<br><br>
* After detecting "person", the user is prompted to enter a "password". <br>
* If the received "password" is the same as the password stored in the system, the user's desired operation is asked as "encode, decode". <br>
* Encode encrypts the data it receives from the user with a "fernet" key and saves it in the "enc_message_file.csv" file. <br>
* The "fernet" key used for encode is also saved in "key.csv". This key is required to be able to open text again during decode. If the user has entered the wrong "password" at first, the system will terminate. <br><br><br>


<hr>
1) "Password" işlemi ( "Password" Operation ) <br>

* <b> Türkçe : </b> "person" sınıfı algılandıktan sonra kullanıcıdan bir "password" istenir. Eğer sistemde kayıtlı "password" ile girilen "password" uyuşmuyorsa sistem sonlanır.  <br>
* <b> English : </b> After the "person" class is detected, the user is prompted for a "password". If the "password" registered in the system and the "password" entered do not match, the system terminates. <br><br>
![1](https://github.com/SeymaAtmaca/YOLOv4_Detection_for_Data_Privacy/blob/main/images/1.jpg ) 

<br><br><br>

2) Encode işlemi ( Encode Operation ) <br>
* <b> Türkçe : <b> Encode işlemi seçildikten sonra kullanıcıdan kaydetmek istediği mesajı girmesi beklenir. Alınan mesaj fernet ile şifrelenerek ilgili dosyalara kaydedilir ve program sonlanır. <br>
* <b> English : <b> After the encode operation is selected, the user is expected to enter the message he wants to record. The received message is encrypted with fernet and saved in the relevant files and the program is terminated. <br><br>
![2](https://github.com/SeymaAtmaca/YOLOv4_Detection_for_Data_Privacy/blob/main/images/2.jpg ) <br><br><br>


3) Decode işlemi ( Decode Operation ) <br>
* <b> Türkçe : <b> Decode işleminde, "enc_message_file.csv" dosyasındaki şifreli mesaj, "fernet.csv" dosyasında depolanan anahtar ile açılır ve kayıtlı mesaj termianlde gösterilir. Bu noktada güvenliği daha da artırabilmek için "key.csv" dosyası farklı bir konumda saklanabilir. <br>
* <b> English : <b> In the decode operation, the encrypted message in the "enc_message_file.csv" file is decrypted with the key stored in the "fernet.csv" file and the recorded message is displayed in the termianl. At this point, the "key.csv" file can be stored in a different location to further increase security. <br><br> 

![3](https://github.com/SeymaAtmaca/YOLOv4_Detection_for_Data_Privacy/blob/main/images/3.jpg )
<br><br><br>


## Technologies
<ul>
<li> Python </li>
</ul>

<br><br>

## Contact

 My [LinkedIn](https://www.linkedin.com/in/%C5%9Feyma-atmaca-925b57195/) profile.
