# Football-Manager-RestApi

                                    Futbol Müsabakası Uygulaması
                                          RestApi Projesi
Amaç: Bir futbol maçı için A ve B takımlarına katılacak futbolcuları seçerek takımları organize 
etmek.

Kurallar: 
• Tüm veri alanları validate edilmelidir. Örn: Email hem format olarak hemde boşluk 
denetimi olarak kontrol edilmelidir.
• Json veri dönüş standartlarına uyulmalıdır. Enum kullanarak geri dönüş key’leri 
standartı sağlanmalıdır.

Sisteme üye olma: Futbolcu ad, soy ad, mail, şifre ve yaş girerek sisteme kayıt olur. Üye 
olurken en az 18 yaş ve üstü kuralı olmalıdır. Bu işlem sonunda futbolcuya üyeliği başarılı 
olmuş ise “fid” id’si verilir.
URL: footballerRegister -> POST

Takıma katılma: Futbolcu kendisi için atanmış “fid” ile hangi takıma üye olacağını belirtir ve o 
takıma girer. Takımlar “A” ve “B” takımı olarak mevcuttur. Bir futbolcu aynı anda bir takıma 
üye olabilir eğer farklı bir takıma daha katılmak isterse uygulama uyarı vermelidir.
URL: teamInsert/A -> POST

Takımları oluşturma: Sistem A ve B takımları için yapılan başvurular sonunda takımları 
oluşturmalıdır. Her takım 11 kişiden oluşmalıdır. Takımlar oluşturulurken yaşları en küçük 
olandan en büyük olana sıralayacak şekilde yapılmalıdır.
URL: teamCreate -> GET
{
A: [],
B: []
}

Yedeklerin oluşturulması: Her takım için eğer varsa fazla başvuru yedek listesi de olmalıdır. 
Yedek listesi 5 kişiden oluşmalı ana takıma atanmamış yine yaşları küçükten büyüye doğru 
sıralayacak şekilde olmalıdır.
URL: backUpCreate -> GET
{
A: [],
B: []
}

![footballer-save](https://user-images.githubusercontent.com/60547236/180998162-4af52c7b-a83c-4bdd-beb9-38070ccbac0d.png)
