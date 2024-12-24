# ICP-internship

Merhaba! Ben, Kocaeli Üniversitesi Bilişim Sistemleri Mühendisliği mezunuyum ve yazılım geliştirme alanında tutkuyla çalışıyorum. Bu projeyi, Motoko programlama dilini öğrenme sürecimde hem kendimi geliştirmek hem de öğrendiklerimi pratiğe dökmek için hazırladım.

Telefon rehberi ve mesajlaşma gibi günlük hayatta karşılaşılan problemleri çözmek, yazılım geliştirme konusundaki motivasyonumu artırdı. 2025 Patika.dev Staj Programı’na hazırlanırken, bu proje sayesinde hem teknik becerilerimi sergiledim hem de analitik düşünme yeteneğimi geliştirdim. Bu sistem, öğrenme yolculuğumun bir ürünü ve gelecekteki projelerim için sağlam bir temel oluşturuyor.

PhoneBook and Messaging System

Bu proje, Motoko programlama diliyle yazılmış temel bir Telefon Rehberi ve Mesajlaşma Sistemi uygulamasıdır. Telefon rehberi yönetimi ve mesaj gönderimi gibi temel özellikleri sağlar; gönderilen mesajlar daha sonra görüntülenmek üzere saklanır.

Özellikler

Telefon Rehberi Yönetimi:
	•	Yeni kişileri detaylarıyla ekleme.
	•	Kişi ismine göre iletişim bilgilerini sorgulama.

Mesajlaşma Sistemi:
	•	Kişilere mesaj gönderme.
	•	Gönderilen mesajların geçmişini gönderenin telefon numarasına göre saklama ve görüntüleme.

Kod Detayları

Veri Yapıları

PhoneBook (Telefon Rehberi):
	•	HashMap kullanılır.
	•	Key (Anahtar): Kişi ismi (Name).
	•	Value (Değer): Kişi detayları (Entry).

Her bir Entry şu bilgileri içerir:
	•	desc: Kişiyle ilgili kısa bir açıklama.
	•	phone: Kişinin telefon numarası.

MessageHistory (Mesaj Geçmişi):
	•	HashMap kullanılır.
	•	Key (Anahtar): Gönderenin telefon numarası (Phone).
	•	Value (Değer): Gönderilen mesaj (Message).

Her bir Message şu bilgileri içerir:
	•	receiver: Mesajın alıcısı.
	•	mess: Mesaj içeriği.

Temel Fonksiyonlar
	1.	insert(name: Name, entry: Entry): async ()
Yeni bir kişiyi telefon rehberine ekler.
	2.	sendMessage(senderPhone: Phone, message: Message): async ()
Mesaj gönderir ve mesaj geçmişine kaydeder.
	3.	getPhone(name: Name): async ?Entry
Verilen isimle eşleşen kişinin iletişim bilgilerini döndürür.
	4.	getMessage(senderPhone: Phone): async ?Message
Belirtilen telefon numarasıyla gönderilen son mesajı döndürür.

Kurulum ve Kullanım

Ön Gereklilikler
	•	Motoko Playground’u kullanın veya yerel makinenizde DFINITY SDK’yı kurun.

Örnek Kullanım
	1.	Telefon Rehberine Yeni Kişi Ekleme:

await Actor.insert("Alice", {desc = "Friend", phone = "123-456-7890"});


	2.	İsimle İletişim Bilgilerini Sorgulama:

let alice = await Actor.getPhone("Alice");
alice; // { desc = "Friend"; phone = "123-456-7890" }


	3.	Gönderenin Alıcıya Mesaj Göndermesi:

await Actor.sendMessage("123-456-7890", {receiver = "Bob", mess = "Hello, Bob!"});


	4.	Telefon Numarasıyla Mesaj Geçmişini Sorgulama:

let messageHistory = await Actor.getMessage("123-456-7890");
messageHistory; // { receiver = "Bob"; mess = "Hello, Bob!" }

Motivasyon

Bu proje, Motoko’da HashMap veri yapısının temel kullanımını ve aktör tabanlı programlamayı göstermek için oluşturuldu. Proje, Motoko’nun güçlü yönlerini sergilemek ve yazılım geliştirme becerilerimi daha ileri seviyeye taşımak için bir adım oldu.
