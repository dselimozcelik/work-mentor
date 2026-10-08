---
description: 'Bir kavram için Selim''e görselli, tek dosyalık HTML ders üret'
agent: 'agent'
---

Bağlam: [KAVRAMLAR.md](../../KAVRAMLAR.md), [ILERLEME.md](../../ILERLEME.md)

Selim bir konuda ders istedi ya da bir kavram sohbette oturmadı. Görevin: o konu için **tek, kısa bir HTML ders** üretmek, açmak, soruları sormak ve Selim'in sohbetteki cevaplarını değerlendirmek. Konu, komuttan sonra yazılan metin. Yazılmadıysa sor.

## Ders dosyası

- Konum: `dersler/NNNN-konu-adi.html`. NNNN, `dersler/` içindeki son numaranın bir fazlası, 4 hane (ilk ders `0001`). Dosya tek başına çalışsın, CSS satır içi olsun, dış bağımlılık olmasın.
- Bitince aç: terminalde `start dersler/NNNN-konu-adi.html` (Windows). Açamazsan dosyanın yolunu Selim'e söyle.
- Ders yaklaşık 5 dakikada okunmalı ve **tek bir kazanım** öğretmeli. Konu büyükse böl: ilk parçayı yaz, devamını sor.
- **Bankaya özgü bilgi yok.** Ders genel kavramı anlatır. Örnek gerekirse uydurma ama gerçekçi bir senaryo kullan (sipariş servisi, ödeme bildirimi gibi) ve "örnek" diye belirt.

## Yapı

1. **Kazanım:** Tek cümle.
2. **Neden önemli:** Kısa. İşte bu kavrama nerede rastlayacağını söyle.
3. **Kavram:** Kısa ve net. Önce ihtiyaç ("bu olmasaydı ne olurdu"), sonra çözüm.
4. **Görsel:** Satır içi SVG ile kutu-ok diyagramı ya da adım adım akış. Selim görselli dersle en iyi öğreniyor. Akış varsa adımları numarala.
5. **Benzetme:** Bildiği bir şeyden, ve benzetmenin bozulduğu yer.
6. **Sorular:** Aşağıdaki kurallara göre.
7. **Kaynaklar:** Aşağıdaki kurallara göre.
8. Son satır: "Takıldığın yer olursa sohbette sor."

## Stil

Selim'in onayladığı bej tema. `color-scheme: light`, **dark mode yok, bembeyaz yok**. Bu CSS'i temel al:

```css
:root { color-scheme: light; --bg:#e9e6dc; --fg:#1d1d1d; --muted:#555; --accent:#a00000; --code-bg:#dcd8c9; --line:#c2bdaa; }
body { background:var(--bg); color:var(--fg); font:18px/1.6 Georgia, "Times New Roman", serif; max-width:42rem; margin:3rem auto; padding:0 1rem; }
h1 { font-size:1.9rem; margin-bottom:.2rem; }
h2 { font-size:1.25rem; margin-top:2.2rem; border-bottom:1px solid var(--line); padding-bottom:.2rem; }
.sub { color:var(--muted); font-style:italic; margin-top:0; }
code, pre { font:15px/1.5 Consolas, "Courier New", monospace; background:var(--code-bg); }
code { padding:.1rem .3rem; }
pre { padding:.8rem 1rem; overflow-x:auto; border-left:3px solid var(--accent); }
a { color:var(--accent); }
svg { display:block; width:100%; height:auto; margin:.2rem 0 .3rem; }
svg .box { fill:#f4f1e7; stroke:#8a846f; stroke-width:1.5; }
svg .tag { fill:#a00000; }
svg text { fill:#1d1d1d; font:13px Consolas, "Courier New", monospace; }
svg text.b { font-weight:bold; }
svg text.w { fill:#fff; font-weight:bold; }
svg .ln { stroke:#555; stroke-width:1.6; fill:none; }
.cap { color:var(--muted); font-size:15px; margin-top:0; }
```

## Sorular

- **2 ya da 3 soru, fazlası değil.** Selim sorulara gömülmek istemiyor.
- **Seviye (Selim'in açık isteği):** Rahatça cevaplayabileceği tanım soruları olmasın. Hedef "senior olma yolu": kıdemli bir mühendisin design review'da, PR incelemesinde ya da mülakatta soracağı türden sorular. Selim'in seviyesinin bir adım üstünü hedefle: tamamen yabancı olmasın ama rahat da olmasın.
- Türler:
  1. **Savun / açıkla:** "Bir ekip arkadaşın 'Kafka zaten bir queue, RabbitMQ'dan farkı yok' diyor. Ona ne dersin, hangi gerekçeyi gösterirsin?"
  2. **Tahmin / ne bozulur:** "Bir consumer mesajı işledi ama offset'i commit etmeden çöktü. Yeniden başladığında ne olur, bu bir ödeme mesajıysa neden tehlikeli?"
  3. **Karar / trade-off:** "Zamanlanmış bir işin üç instance'ta aynı anda çalışmasını ShedLock'la engelliyoruz. Lock süresi işin süresinden kısa kalırsa ne olur, neyi feda ederek uzun tutarız?"
- Yazmadan önce her soruyu sına: Cevap dersten kopyalanabiliyor mu? Yanlış bir cevap hangi yanılgıdan geldiğini ortaya çıkarır mı? Tek kelimeyle cevaplanıyor mu? Selim bunu zaten rahatça cevaplar mı? Sorun varsa soruyu yeniden yaz.
- **Cevap anahtarı HTML'de olmaz.** Sorular sadece listelenir.

## Kaynaklar

- Uydurma kaynak yok. Sadece emin olduğun resmi dokümanları (Apache Kafka docs, grpc.io, Spring docs, ShedLock'un GitHub README'si) ve yerleşik kaynakları (Baeldung gibi) öner. Linki doğrulayabiliyorsan (fetch aracı varsa) doğrula.
- **2-3 video öner**, çok izlenen ve saygın kanallardan (ör. Confluent, ByteByteGo, Hussein Nasser). Linkinden emin değilsen link uydurma: kanal adını ve YouTube'da aratılacak başlığı yaz. İzlenme sayısını bilmiyorsan yazma.
- Selim İngilizce kaynağı rahat okuyor.

## Cevapları değerlendirme

- Selim cevaplarını sohbette yazar. Her cevap için net geri bildirim ver: neyi doğru yaptı, neyi eksik ya da yanlış. Pohpohlama yok, "zayıf ama olur" yok.
- Yanlışı düzeltirken cevabı hazır verme, önce yönlendirici bir soru sor. Eksik olan saf bir bilgiyse kısaca söyle.
- Cevap iyiyse nedenini söyle ve bir adım ileri götür (alternatif, uç durum).
- Bitince `KAVRAMLAR.md`'de kavramın seviyesini cevaplara göre güncelle.
