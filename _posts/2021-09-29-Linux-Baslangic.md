---
title: Linux'a Başlarken
author: Ozgur Ozan Cakmak
date: 2021-09-29 19:00:00 +0300
categories: [Sibergüvenlik]
tags: [Sibergüvenlik, TryHackMe, Linux]


---

# Linux'a Başlarken

**Kaynak:** https://tryhackme.com/room/linuxfundamentalspart1

## Giriş

Sibergüvenlik konusunda kullandığımız ana araçlar genel olarak Linux dağıtımları oluyor. Bu alanda en popüler iki dağıtım:

- Kali
- Parrot

olarak ifade edilebilir. 

Bu yazı serisi dahilinde, kaynak olarak aldığım odadakinin aksine, daha yavaş gideceğiz. Ben şahsen komut satırında arama yaparken kullandığımız `find` ve `grep` komutlarının kendi başına bir yazıyı hakettiğini düşünüyorum.

## Terminal

Sibergüvenlik araçlarından bahsetmişken bu araçların bazıları (hatta çoğu demek daha doğru olabilir) herhangi bir görsel arabirime sahip olmayacaklar. Dolayısıyla **terminal** olarak adlandırdığımız komut satırından çalıştırıyor olacağız. 

İlk komutumuz, ardından gelen şeyi ekrana yazan `echo` komutu olacak. Bir klasik olarak `Merhaba Dünya` yazalım:

	echo "Merhaba Dünya"

Bu komudu yazıp `Enter`'a bastığımızda 

	Merhaba Dünya

yazdığını göreceğiz.

### Kimim Ben?

Gelelim az önce bahsettiğim kullanıcımızın kim olduğuna bakmaya. Bu komut İngilizce'deki "kimim ben" cümlenin bitişik hali olacak:

	whoami

Eğer kali üstünden kullanıyorsanız size

	kali

diye yanıt verdiğini göreceksiniz.

## Dosya Sistemi Operasyonları
Gelelim işin daha interaktif kısımlarına. Windows altında komut satırı kullandıysanız oradaki eşlenikleri ile beraber yazalım:

Linux Komutu | Windows Komutu | Anlamı
-|-|-
`ls` | `dir` | İçinde bulunduğumuz "klasörün" dosyalarını listeler
`cd` | `cd` | Klasör değiştirimi için kullanılır
`cat` | `type` | Dosyaların içeriğini ekrana basmak için kullanılır
`pwd` | `echo %cd%` veya PowerShell içinde `Get-Location` | İçinde bulunduğumuz noktanın yerini ekrana basar.

Daha detaylı bakalım

### ls - Dosya Listeleme
İçinde bulunduğumuz klasörün dosyalarını listelemek için

	ls

yazmamız yeterlidir. Bu komut aynı zamanda başka yerdeki dosyaları da listeleyebilir:
	
	ls # içinde bulunduğumuz klasördeki dosyaları listeler
	ls Documents # İçinde bulunduğumuz klasörün içinde Documents diye bir klasör varsa onun dosyaları listelenir

### cd - Klasör değiştirimi
`cd` komutu aslında `ls` ile beraber kullanılan en önemli komutlardan birisidir. `ls` ile bulunduğumuz noktayı görüyorsak, `cd` ile başka yere yürüyoruz diyebilirim. 

	cd Documents

içinde bulunduğumuz yerde `Documents` adında bir klasör varsa oraya "gitmemizi" sağlar. Bu noktada

	ls

komutu bize `Documents`'in içini listeleyecektir!

### cat - Dosya içeriğini ekrana basma
Dosyaları listelemek güzel olsa da bu dosyaların içinde ne yazdığını görebilmek de önemli bir şeydir. Nitekim `cat` komutu tam da bunu yapar.

	cat not.txt

komutu eğer içinde bulunduğumuz klasörde `not.txt` diye bir dosya varsa onun içini ekrana basar. 

### pwd - İçinde bulunduğumuz klasörün yerini öğrenmece
Son olarak `pwd` komutu içinde bulunduğumuz klasörün yerini ekrana basar. Mesela Linux altında Ozgur kullanıcısının Documents'i içinde olduğumuzu varsayalım.

	pwd

dediğimizde ekrana

	/home/Ozgur/Documents

gelir. Bu işaretleme Linux'un dosya yapısını da bize özetler aslında. Linux'ta, Windows'ta olduğu gibi `C:/` diye bir kullanım yoktur. Harddisk'in en üstünü ifade eden şey burada `/` simgesidir ve kök anlamına gelir. Yani metinsel olarak ifade edersek

	/ # Kök
	----home # Kullanıcıların klasörlerinin olduğu yer
	--------Ozgur # Ozgur kullanıcısının dosyaları
	------------Documents # Ozgur'un Documents klasörü <----

Burada mesela 

	cd ..

dersem bir üst klasöre çıkarım:

	/ # Kök
	----home # Kullanıcıların klasörlerinin olduğu yer
	--------Ozgur # Ozgur kullanıcısının dosyaları <----


Okuduğunuz için teşekkür ederim.