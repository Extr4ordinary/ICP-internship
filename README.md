# ICP-internship

# 📞 PhoneBook and Messaging System

**Merhaba!**  
Ben, Kocaeli Üniversitesi Bilişim Sistemleri Mühendisliği mezunuyum ve yazılım geliştirme alanında tutkuyla çalışıyorum. Bu projeyi, **Motoko programlama dili** öğrenme sürecimde hem kendimi geliştirmek hem de öğrendiklerimi pratiğe dökmek için hazırladım.  

Telefon rehberi ve mesajlaşma gibi günlük hayatın basit ama vazgeçilmez problemlerini ele almak, yazılım geliştirme konusundaki motivasyonumu daha da artırdı. ✨  
Bu proje, **2025 Patika.dev Staj Programı** için hazırlık sürecimde analitik düşünme yeteneklerimi geliştirme ve teknik becerilerimi sergileme amacıyla oluşturulmuştur.  

---

## 🚀 **Proje Hakkında**

Bu proje, Motoko programlama diliyle yazılmış temel bir **Telefon Rehberi ve Mesajlaşma Sistemi** uygulamasıdır. Projenin amacı, günlük hayatta sıkça kullanılan bir sistemi basit ama etkili bir şekilde uygulayarak yazılım geliştirme prensiplerini öğrenmek ve sergilemektir.

---

### 🛠️ **Özellikler**

#### 📒 Telefon Rehberi Yönetimi:
- Yeni kişileri detaylarıyla ekleyin.  
- Kişi ismine göre iletişim bilgilerini sorgulayın.  

#### 💬 Mesajlaşma Sistemi:
- Kişilere mesaj gönderin.  
- Gönderilen mesajların geçmişini gönderenin telefon numarasına göre saklayın ve görüntüleyin.  

---

### 🔍 **Kod Detayları**

#### **Veri Yapıları**

📂 **PhoneBook (Telefon Rehberi)**  
- **HashMap** veri yapısı kullanılır.  
- **Key (Anahtar):** Kişi ismi (Name).  
- **Value (Değer):** Kişi detayları (Entry).  

Her bir `Entry` şu bilgileri içerir:  
- `desc`: Kişiyle ilgili kısa bir açıklama.  
- `phone`: Kişinin telefon numarası.  

📂 **MessageHistory (Mesaj Geçmişi)**  
- **HashMap** veri yapısı kullanılır.  
- **Key (Anahtar):** Gönderenin telefon numarası (Phone).  
- **Value (Değer):** Gönderilen mesaj (Message).  

Her bir `Message` şu bilgileri içerir:  
- `receiver`: Mesajın alıcısı.  
- `mess`: Mesaj içeriği.  

---

### ✨ **Temel Fonksiyonlar**

1. **`insert(name: Name, entry: Entry): async ()`**  
   Yeni bir kişiyi telefon rehberine ekler.

2. **`sendMessage(senderPhone: Phone, message: Message): async ()`**  
   Mesaj gönderir ve mesaj geçmişine kaydeder.

3. **`getPhone(name: Name): async ?Entry`**  
   Verilen isimle eşleşen kişinin iletişim bilgilerini döndürür.

4. **`getMessage(senderPhone: Phone): async ?Message`**  
   Belirtilen telefon numarasıyla gönderilen son mesajı döndürür.

---

## 🛠️ **Nasıl Kullanılır?**

### ⚙️ **Gereksinimler**
- Motoko Playground veya **DFINITY SDK** kurulu olmalıdır.

### 🧑‍💻 **Örnek Kullanım**
Yeni bir kişiyi eklemek:  
```motoko
await Actor.insert("Alice", {desc = "Friend", phone = "123-456-7890"})
Belirtilen telefon numarasıyla gönderilen son mesajı döndürür.




