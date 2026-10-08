---
description: 'Teknik bir dokümanı Selim ile bölüm bölüm birlikte oku'
agent: 'agent'
---

Bağlam: [ILERLEME.md](../../ILERLEME.md), [KAVRAMLAR.md](../../KAVRAMLAR.md)

Selim bir teknik dokümanı seninle birlikte okumak istiyor. Doküman `docs/` altında bir dosya olabilir, sohbete eklenmiş ya da yapıştırılmış da olabilir. Hangisi olduğu belli değilse sor.

`ILERLEME.md`'de yarım kalmış bir okuma varsa `docs/<doküman-adi>-notlar.md` dosyasına bak ve kaldığınız parçadan devam et.

Selim "hızlı" derse parça sonlarındaki soruları atla, sadece anlat.

## 0. Neden okuyor?

Selim söylemediyse önce tek bir soru sor: "Bu dokümanı bir task için mi okuyorsun, yoksa sistemi genel olarak anlamak için mi?" Task içinse o task'a dokunan parçaları öne al ve daha derin anlat.

## 1. Büyük resim (ilk mesaj)

Dokümanın tamamını oku, ama hepsini anlatma. Tek mesajda şunları ver:

- **Problem:** Bu sistem hangi problemi çözüyor? 2-3 sade cümle.
- **Akış diyagramı:** Ana parçalar ve aralarındaki akışı gösteren tek bir ASCII kutu-ok diyagramı. Okların üzerine ne aktığını yaz (event, gRPC çağrısı, DB yazma, zamanlanmış iş...). En fazla 6-7 kutu.
- **Okuma planı:** Dokümanı 4-8 parçaya böl. Dokümanın kendi bölüm sırasına uymak zorunda değilsin, akışa göre sırala: önce ana akış (mutlu yol), sonra ayrıntılar, hata durumları, operasyon ve konfigürasyon. Her parçaya bir numara ve tek satırlık bir başlık ver.
- **Gerekecek kavramlar:** Dokümanda geçen ve `KAVRAMLAR.md`'de seviyesi düşük olan kavramların sadece adlarını listele. Akışı anlamak için şart olanları işaretle.

Sonunda sor: "Bu resim sana anlamlı geliyor mu? 1. parçadan başlayalım mı?"

## 2. Her parça (bir mesajda bir parça)

1. **Nerede duruyoruz:** Büyük diyagramı ya da ilgili kısmını tekrar göster, şu anki parçayı işaretle (örneğin `>>> [Kafka] <<<`).
2. **Ne diyor:** Parçanın anlattığını kısa paragraflarla, sade Türkçeyle aktar. Dokümanın dili ağırsa cümleyi "yani..." diye aç.
3. **Yeni kavramlar:** Parçada geçen ve Selim'in bilmediği kavramları `KAVRAMLAR.md`'ye bakarak belirle. Her birini 2-4 cümleyle anlat ve bildiği bir şeyden benzetme kur. Kavram büyükse burada kısa tut, `/kavram` ya da `/ders` öner.
4. **Akış izi (en önemli adım):** Somut bir örnekle (örnek bir istek ya da mesaj) adım adım "önce şu olur, sonra şu" diye izle. Selim tanımları biliyor ama akışı görmekte zorlanıyor.
5. **Tek soru:** Parçayı anladığını gösterecek tek bir soru sor. Tanım sorusu sorma. İyi türler: "Bu adım başarısız olursa ne olur?", "Burada neden X kullanılmış da Y değil?", "Bu mesaj hangi sırayla nereye gidiyor, kendi cümlenle anlat." Cevabı bekle, net geri bildirim ver, sonra sıradaki parçaya geç.

Doküman bir şeyi söyleyip sebebini söylemiyorsa bunu belirt. Doküman eksik ya da çelişkiliyse işaretle ve "mentoruna sorulacaklar" listesine ekle. Selim bu soruları işteki mentoruna götürmek istiyor.

## 3. Notlar

Her parça bitince `docs/<doküman-adi>-notlar.md` dosyasını güncelle. İçinde şunlar olsun: büyük diyagram, okuma planı (biten parçalar ✓ ile işaretli), Selim'in kendi cümleleriyle her parçanın 2-3 satırlık özeti ve mentora sorulacaklar. Bu dosya git'e girmez, bankaya özgü bilgi burada durabilir.

## 4. Bitiş

Bütün parçalar bitince Selim'den akışın tamamını kendi cümleleriyle anlatmasını iste (istersen kendi diyagramını çizebilir). Bu, "anladım" ile "anlatabiliyorum" arasındaki farkı ölçer. Anlatımı değerlendir, eksikleri söyle.
