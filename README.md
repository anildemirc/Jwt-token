JWT Token nedir? 
JWT (JSON Web Token), veri transferini güvenli bir şekilde sağlamak ve kullanıcının bilgilerini doğrulamak için kullanılan, JSON formatındaki bir standarttır.

JWT Yapısı nasıldır?
JWT’ler, header (başlık), payload (yük) ve signature (imza) olmak üzere üç bileşenden oluşur.

![jwtio-encoding-example](https://github.com/user-attachments/assets/b98bccce-d35b-4b9a-9034-bfb54cda540d)
1. Header (Başlık):
JWT’nin türünü (typ) ve kullanılan şifreleme algoritmasını (alg) belirtir.

2. Payload (Yük):
Payload, JWT içinde saklanması istenen verileri içerir. Bu veriler, kullanıcıya özgü bilgiler, talepler veya diğer verilerden oluşur.

3. Signature (İmza)
Signature, JWT’nin güvenilirliğini sağlamak için kullanılan bir dijital imzadır. Bu imza sayesinde, JWT’nin değiştirilmediği ve güvenli olduğu kontrol edilir.

JWT Kullanımı

1. Token Oluşturma
Sunucu, kullanıcının kimlik bilgilerini doğrular ve bir JWT oluşturur. Oluşturulan JWT, header, payload ve signature kısımlarını içerir.

2. Token İletimi
Sunucu, oluşturulan JWT’yi browser’a ileterek kullanıcıya yanıt verir. Browser, her isteği Authorization başlığı altında JWT ile sunucuya gönderir.

3. Token Doğrulama
Sunucu, her gelen isteği doğrulamak için JWT’nin imzasını kontrol eder. İmza doğrulandığında, sunucu JWT içindeki kullanıcı bilgilerini kullanarak talebi işler. İmza doğrulanamazsa veya JWT süresi dolmuşsa sunucu hata mesajı veya uygun yanıt gönderir.


![workflow_jwt](https://github.com/user-attachments/assets/24c12453-e544-4ae6-b950-c668c00687b7)
