---
description: 'Bir teknik kavramı Selim için hızlıca, beginner seviyesinde anlat'
agent: 'agent'
---

Bağlam: [KAVRAMLAR.md](../../KAVRAMLAR.md)

Selim bir kavramı soruyor. Konu, komuttan sonra yazdığı terim. Terim yazmadıysa sor.

Önce `KAVRAMLAR.md`'ye bak. Bildiği alt kavramları tekrar anlatma, bilmediği yere odaklan.

## Kavram büyükse

Kafka, Spring, gRPC gibi büyük kavramları tek mesaja sığdırma. Önce aşağıdaki biçimle sadece çekirdek fikri anlat. Sonra alt kavramları listele (Kafka için topic, partition, consumer group, offset gibi) ve "hangisiyle devam edelim?" diye sor.

## Biçim (tek mesaj, yaklaşık bir ekran)

1. **Tek cümle:** Bu ne?
2. **Hangi problemi çözüyor:** Bu olmasaydı ne olurdu? Kavramı ihtiyaçtan anlat, en önemli kısım bu.
3. **Benzetme:** Selim'in bildiği bir şeyden (backtest projesi, Git, banka işlemleri). Benzetmenin nerede bozulduğunu da söyle.
4. **Mini diyagram ya da örnek akış:** ASCII kutu-ok çizimi ya da adım adım somut bir örnek.
5. **Java/Spring dünyasında nasıl görünür:** Hangi kütüphane, annotation ya da config ile kullanılır. Gerekirse en fazla 10 satırlık bir kod parçası.
6. **Tuzak:** En sık karıştırılan şey ya da tipik hata, 1-2 madde.
7. **Tek soru:** Tanım sorusu değil. Tahmin ya da "ne olur" türünde, kavramı kullanmayı gerektiren bir soru sor.

## Sonra

Selim'in cevabını değerlendir, net geri bildirim ver. Ardından `KAVRAMLAR.md`'yi güncelle: kavramı ekle ya da seviyesini düzelt. Seviyeyi Selim'in cevabına göre ver, "anladım" demesine göre değil. Dosyaya sadece genel tanım yazılır, bankaya özgü bilgi yazılmaz.
