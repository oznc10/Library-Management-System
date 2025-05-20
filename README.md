# 📚 Library Management System

This is a simple **Library Management System** project developed in Java for educational purposes. It allows users to add various types of media (books, movies, music albums), manage members, and process borrow/return operations with proper data consistency and exception handling.

> 🏫 This project was prepared as part of a course assignment for **Akdeniz University, Department of Computer Science Engineering**.  
> Special thanks to the instructors and assistants who designed and supervised this assignment.

---

## ⚙️ Features

- 📖 Manage different types of media:
  - Book (`Book`)
  - Movie (`Movie`)
  - Music Album (`MusicAlbum`)
- 👥 Member operations: add, remove, search
- 📥 Borrow & 📤 Return media with restrictions
- 🚫 Exception handling for error scenarios
- 🧪 Built-in test suite in `MainProgram.java`

---

## 🧱 Structures & Design

### 📦 Object-Oriented Design
- `Media` (abstract) superclass with concrete implementations:
  - `Book`, `Movie`, `MusicAlbum`
- `Member` class to manage users and their borrowed media
- `LibraryManagement` class as the central controller

### 🧩 Interface
- `Borrowable` interface defines borrowable items

### 🗂️ Data Collections
- `HashMap<String, Media>` → media collection
- `HashMap<String, Member>` → member directory
- `ArrayList<Borrowable>` → list of borrowed items per member

### 🚨 Custom Exceptions
- `MediaAlreadyExistsException`
- `MediaNotFoundException`
- `MemberAlreadyExistsException`
- `MemberNotFoundException`
- `CannotBorrowException`
- `CannotReturnException`

---

## ✅ Highlights
- Error messages are **context-sensitive**. For example, if a member is not found during removal, the message includes `"not found for removal"` to clarify the operation with rethrowing Exception.
- ⚠️ **Note:** In some test outputs, error messages may appear out of order. This happens because `System.err` and `System.out` use separate buffers. This is a known behavior in Java. Although `System.err.flush()` can help, it may not guarantee perfect order in some IDEs or terminals.

---

## ▶️ How to Run

1. Open the project in your preferred Java IDE.
2. Run `MainProgram.java`.
3. All functionalities will be demonstrated through structured test cases in the console output.

---

## 🧪 Test Coverage

The test suite in `MainProgram.java` includes:

- Adding and removing media
- Adding and removing members
- Borrowing and returning items
- Error handling for duplicate, missing, or invalid operations
- Listing current media and borrowed items

---

## 🙏 Acknowledgement

This project was developed as an assignment under the guidance of faculty at **Akdeniz University, Department of Computer Science Engineering**.  
Special thanks to the professors and assistants who contributed to the preparation of the coursework and test cases.

---

## 👤 Author

**Name:** Ömer Özenç  
**Department:** Computer Science Engineering  
**University:** Akdeniz University

---
# 📚 Kütüphane Yönetim Sistemi

Bu proje, Java programlama dili ile geliştirilen basit bir **Kütüphane Yönetim Sistemi**dir. Kitap, film ve müzik albümü gibi medya öğeleri eklenebilir, üyeler yönetilebilir ve bu üyelerin ödünç alma–iade işlemleri gerçekleştirilebilir. Proje, veri tutarlılığı ve özel hata yönetimi ile birlikte tasarlanmıştır.

> 🏫 Bu proje, **Akdeniz Üniversitesi Bilgisayar Mühendisliği Bölümü** kapsamında verilen bir ders ödevi olarak hazırlanmıştır.  
> Ödevi hazırlayan değerli hocalarımıza ve asistanlara teşekkür ederim.

---

## ⚙️ Özellikler

- 📖 Farklı medya türlerini yönetme:
  - Kitap (`Book`)
  - Film (`Movie`)
  - Müzik Albümü (`MusicAlbum`)
- 👥 Üye işlemleri: ekleme, silme, arama
- 📥 Ödünç alma & 📤 iade etme işlemleri
- 🚫 Hatalı işlemler için özel exception yapısı
- 🧪 `MainProgram.java` içinde yer alan kapsamlı test senaryoları

---

## 🧱 Yapılar ve Tasarım

### 📦 Nesne Yönelimli Tasarım
- `Media` (soyut sınıf) → `Book`, `Movie`, `MusicAlbum`
- `Member` sınıfı: üyeleri ve borrowed listelerini yönetir
- `LibraryManagement`: tüm sistemi yöneten merkez sınıf

### 🧩 Arayüzler
- `Borrowable`: ödünç alınabilir medya öğeleri için tanımlı arayüz

### 🗂️ Koleksiyonlar
- `HashMap<String, Media>` → medya koleksiyonu
- `HashMap<String, Member>` → üye dizini
- `ArrayList<Borrowable>` → her üyenin ödünç aldığı öğeler

### 🚨 Özel Hata Türleri (Exception'lar)
- `MediaAlreadyExistsException`
- `MediaNotFoundException`
- `MemberAlreadyExistsException`
- `MemberNotFoundException`
- `CannotBorrowException`
- `CannotReturnException`

---

## ✅ Dikkat Çeken Noktalar

- Hata mesajları **bağlama (context)** özel olarak özelleştirilmiştir. Örneğin, bir üye `removeMember()` içinde bulunamazsa mesajda `"not found for removal"` ifadesi yer alır.Bu yapı Exception'u rethrow'layarak sağlandı.
- ⚠️ **Not:** Bazı hata mesajlarının terminalde doğru sırayla çıkmaması, Java’nın `System.err` ve `System.out` akışlarının tamponlama farkından kaynaklanmaktadır. Bu davranışı azaltmak için `System.err.flush()` denenmiş olsa da, bazı IDE'lerde sıralama garantisi verilmez.

---

## ▶️ Nasıl Çalıştırılır?

1. Projeyi herhangi bir Java IDE'sinde (IntelliJ IDEA, Eclipse, vs.) açın.
2. `MainProgram.java` dosyasını çalıştırın.
3. Tüm test senaryoları terminal üzerinden gözlemlenebilir.

---

## 🧪 Test Kapsamı

`MainProgram.java` dosyasında şunlar test edilmektedir:

- Medya ve üye ekleme
- Aynı ID ile tekrar ekleme (beklenen hata)
- Ödünç alma ve iade işlemleri
- Hatalı işlemlerin test edilmesi
- Mevcut medya ve ödünç alınanların listelenmesi

---

## 🙏 Teşekkür

Bu proje, **Akdeniz Üniversitesi Bilgisayar Mühendisliği Bölümü** kapsamında verilen bir ödev olarak geliştirilmiştir.  
Dersi yürüten değerli hocalarımıza ve test senaryolarını hazırlayan asistanlara teşekkür ederim.

---

## 👤 Geliştirici Bilgisi

**İsim:** Ömer Özenç  
**Bölüm:** Bilgisayar Mühendisliği  
**Üniversite:** Akdeniz Üniversitesi

---
