# Şirket bilgisayarında kurulum

## 0. Önce kural

Bir iç dokümanı Copilot'a okutmanın şirketin onaylı kullanımı içinde olduğundan emin ol. Şirket lisanslı Copilot genelde bunun için verilir, ama emin değilsen ekibine ya da mentoruna sor. Bu repoya bankaya ait bilgi girmez (bkz. `.gitignore`: `docs/`).

## 1. Gerekenler

- VS Code
- GitHub Copilot ve GitHub Copilot Chat eklentileri, şirket hesabıyla giriş yapılmış
- Git

## 2. Repoyu al

OneDrive gibi senkronize edilen bir klasöre koyma.

```
git clone https://github.com/dselimozcelik/work-mentor.git
```

Şirket ağı kişisel GitHub'ı engelliyorsa bu klasörü başka bir yolla taşı ve repo orada sadece yerel kalsın.

## 3. VS Code'da aç

- `File > Open Folder` ile **`work-mentor` klasörünün kendisini** aç. Kök klasör bu olmalı, yoksa Copilot `.github/` altındaki dosyaları okumaz.
- Settings'te şu iki ayarın açık olduğunu kontrol et (genelde varsayılan olarak açıktır, şirket kapatmış olabilir):
  - `github.copilot.chat.codeGeneration.useInstructionFiles`
  - `chat.promptFiles`
- Chat panelinde modu **Agent** yap. Copilot'un `ILERLEME.md` ve `KAVRAMLAR.md` dosyalarını güncelleyebilmesi buna bağlı.

## 4. Dene

Chat'e `/basla` yaz.

- `/` yazınca komutlar (`basla`, `oku`, `kavram`, `ders`, `bitir`) listede görünmüyorsa: prompt files kapalı ya da VS Code eski. Eski sürümlerde prompt dosyalarının başındaki `agent: 'agent'` satırı `mode: 'agent'` olarak yazılıyordu.
- Copilot seni tanımıyor gibi davranıyorsa: chat'te "Bu yanıtta hangi instruction dosyalarını kullandın?" diye sor ya da yanıttaki "References" kısmında `copilot-instructions.md` var mı bak.

## 5. Doküman nasıl verilir

- Dokümanı `docs/` klasörüne koy. Bu klasör git'e girmez.
- Confluence sayfasıysa: içeriği kopyala ve `docs/<kisa-ad>.md` olarak kaydet.
- PDF ise: metne çevir ya da bölüm bölüm sohbete yapıştır.
- Sonra `/oku docs/<kisa-ad>.md` yaz.

## 6. Her oturum

1. `git pull`
2. `/basla`
3. Çalış (`/oku`, `/kavram`, `/ders`)
4. `/bitir`, ardından commit ve `git push`
