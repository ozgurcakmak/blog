---
title: Sibergüvenliğe Giriş
author: Ozgur Ozan Cakmak
date: 2021-09-22 19:00:00 +0300
categories: [Sibergüvenlik]
tags: [Sibergüvenlik, TryHackMe]

---

# Giriş

Efendim merhabalar. Bu yazı serisine hem TryHackMe üzerinde yaptığım notları temize çekmek ve tekrarlamak hem de belki birilerine biraz olsun faydam olur niyetiyle başlıyorum. Her yazının sonunda o yazının temele aldığı TryHackMe odasının linkini bırakıyor olacağım. 

# Sibergüvenliğe Giriş

**Kaynak:** https://tryhackme.com/room/startingoutincybersec

Sibergüvenlik denildiğinde iki ana kariyer yolu vardır denilebilir:

- Saldırı
- Savunma

## Saldırı - Offensive Security

Bu alan çeşitli uygulamalar ve teknolojilere "saldırarak" zaafiyet bulmayı hedefler. Eğer çocukken elektronik aletlerin içini açıp kurcalayarak nasıl çalıştıklarını merak ettiyseniz (ve doğru topladıysanız tekrardan), tabancanın sesini çıkartan aparatı başka bir yere bağlayarak hırsız alarmı falan yaptıysanız tam sizlik bir alan denilebilir. 

Bu alandaki en yaygın iş **sızma testçisi** (penetration tester)'dir. Bu kişiler kurum veya kuruluşlar tarafından kendi ürünlerindeki zaafiyetleri bulmak için çalıştırılırlar. Bu da genelde web uygulamaları veya ağ cihazlarını konu alır.

Bunu yapabilmek için de 

- Programlama - Temel düzeyde de olsa
- Ağ ve Ağ güvenliği 
- Web uygulamalarının nasıl çalıştığı, güvenlik mekanizmaları

konularına hakim olmak gerekir. 

## Savunma - Defensive Security

Saldırı varsa savunma da hemen ardından geliyor tabii ki. Bu alanda ise yine zaafiyet bulmaya ve/veya yazılım ve donanımlardaki ayar sorunlarını bulmaya ve bu alanlardan bize gelecek saldırıları durdurmayı hedefleriz.

Nitekim **Güvenlik Analisti** (Security Analyst) tam da bu işi yapar. Bu kişi çalıştığı kurumdaki sistemleri gözlemleyerek herhangi bir saldırı olup olmadığını tespit etmeye çalışır. Bu tespiti yapabilmenin yolu da doğal olarak bu zımbırtıların nasıl çalıştığını, normal davranışlarını falan bilmekten geçer. Buna ek olarak da bunlara yapılan saldırıların da nasıl olduğunu bilmeniz gerekir ki durumu farkedesiniz.

Bu işe ek olarak **Olay İnceleyicisi** (Incident Responder) olmak da mümkündür. Bu arkadaşlar saldırı olduktan sonra, nasıl ki adli tıptaki olay yeri inceleme ekibi suç mahalline gelir - saldırganın neler yaptığını ve bu eylemlerin kuruma olan etkisi veya etkilerini inceleyerek rapor verirler. Güvenlik analistlerine benzer biçimde sistemlerin nasıl çalıştığını bilmeleri ve saldırganların bıraktığı kanıtları analiz edebilmeleri beklenir. 

Son olarak da **Kötü Yazılım Analizi** (Malware Analysis) vardır. Bu iş kolunda ise kötü niyetli aktörlerin saldırılarında kullandıkları yazılımları inceleyerek anlamaya çalışır ve bu sayede hem daha sonraki saldırıları engellemeye, hem de bazen bu yazılımı kimin ürettiğini tespit etmeyi hedefleriz. 

