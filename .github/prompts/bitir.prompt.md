---
description: 'Oturumu bitir: ILERLEME.md ve KAVRAMLAR.md dosyalarını güncelle'
agent: 'agent'
---

Bağlam: [ILERLEME.md](../../ILERLEME.md), [KAVRAMLAR.md](../../KAVRAMLAR.md)

Selim oturumu bitiriyor. Sırayla şunları yap:

1. **`ILERLEME.md`'yi güncelle.** Tarihi yaz. "Nerede kaldık" kısmını, bir sonraki oturum hiçbir şey hatırlamadan devam edebilecek kadar net yaz. Bu oturumda oturan kavramları, zorlandığı yerleri (ne oldu, ne işe yaradı) ve tekrar sorulacak konuları ekle. Eskimiş bilgiyi sil ya da düzelt.
2. **`KAVRAMLAR.md`'yi güncelle.** Seviyeyi değiştirmek için kanıt, Selim'in kendi anlatımı olmalı. "Anladım" demesi seviye yükseltmez.
3. **Güvenlik kontrolü.** Yazdıklarını yeniden oku. Bankaya özgü bir bilgi (sistem ya da servis adı, topic, tablo, URL, kod) geçtiyse genelleştir. Ayrıntı `docs/` altındaki notlarda kalabilir.
4. **Selim'e göster.** Ne yazdığını kısaca özetle.
5. **Commit.** Commit mesajını hazır ver: İngilizce, fiille başlayan, kısa, tek satır. Komutları Selim çalıştırır:
   ```
   git status
   git add ILERLEME.md KAVRAMLAR.md dersler/
   git commit -m "<mesaj>"
   git push
   ```
