# Telefon Rehberi Projesi

Bu proje, Mo (Motoko) dilinde yazılmış bir telefon rehberi ve mesajlaşma sistemini içermektedir. Kullanıcılar, telefon rehberine kişi ekleyebilir ve mesaj gönderebilirler. Ayrıca, gönderilen mesajların geçmişine ulaşılabilir.

## Özellikler

- *Telefon Rehberi*: Kullanıcılar, ad ve telefon numarası ile kişileri telefon rehberine ekleyebilir.
- *Mesaj Gönderme*: Kullanıcılar, telefon numarası ile mesaj gönderilebilir ve gönderilen mesajlar kaydedilir.
- *Mesaj Geçmişi*: Kullanıcılar, kendi telefon numaraları ile gönderilen mesajların geçmişini görüntüleyebilir.

## Teknolojiler

Bu proje, *Motoko* dilinde yazılmıştır ve *DFINITY* platformunda çalışmaktadır.

## Kullanım

### Telefon Rehberine Kişi Ekleme
Telefon rehberine yeni bir kişi eklemek için insert(name, entry) fonksiyonu kullanılır. Bu fonksiyon, bir isim ve kişi bilgileri (açıklama ve telefon numarası) alır.

motoko
insert("Ali", { desc = "Arkadaş", phone = "1234567890" });


### Telefon Numarasını Alma
Belirli bir kişinin telefon numarasını almak için getPhone(name) fonksiyonu kullanılır.

motoko
let person = getPhone("Ali");


### Mesaj Gönderme
Bir kullanıcı, telefon numarası ve mesaj içeriği ile bir mesaj gönderebilir. Gönderilen mesaj, mesaj geçmişine kaydedilir.

motoko
sendMessage("1234567890", { receiver = "9876543210", mess = "Merhaba!" });


### Gönderilen Mesajları Görüntüleme
Bir kullanıcının gönderdiği mesajları görüntülemek için sentMessages(senderPhone) fonksiyonu kullanılır.

motoko
let messages = sentMessages("1234567890");


## Kurulum

1. Bu projeyi çalıştırmak için *Motoko SDK*'sını kurmanız gerekmektedir.
2. DFINITY internet bilgisayarına dağıtım yapabilmek için DFINITY CLI aracını kullanabilirsiniz.

## Katkı

Katkı yapmak isterseniz, lütfen bir pull request açın. Her türlü katkıya açıktır.

## Lisans

Bu proje, [MIT Lisansı](LICENSE) altında lisanslanmıştır.

---

Yukarıdaki metin, GitHub'da projenizin amacını ve nasıl kullanılacağını net bir şekilde açıklamaya yardımcı olacaktır. Kendi projenize özel eklemeler yaparak bu yapıyı özelleştirebilirsiniz.
