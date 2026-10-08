# Kurulum

## 1. Gerekenler

- VS Code
- GitHub Copilot ve GitHub Copilot Chat eklentileri

## 2. İlk kurulum

1. Repoyu zip olarak indir ve aç. Klasörün adını `work-mentor` yap (zip genelde `work-mentor-main` diye açılır).
2. İçinde `.github` klasörünün olduğunu kontrol et. Gizli görünebilir, Explorer'da "Gizli öğeler"i aç.

## 3. VS Code'da aç

- `File > Open Folder` ile **`work-mentor` klasörünün kendisini** aç. Kök klasör bu olmalı, yoksa Copilot `.github/` altındaki dosyaları okumaz.
- Settings'te şu iki ayarın açık olduğunu kontrol et (genelde varsayılan olarak açıktır):
  - `github.copilot.chat.codeGeneration.useInstructionFiles`
  - `chat.promptFiles`
- Chat panelinde modu **Agent** yap. Copilot'un `ILERLEME.md` ve `KAVRAMLAR.md` dosyalarını güncelleyebilmesi buna bağlı.

## 4. Dene

Chat'e `/basla` yaz.

- `/` yazınca komutlar (`basla`, `oku`, `kavram`, `ders`, `bitir`) listede görünmüyorsa: prompt files kapalı ya da VS Code eski. Eski sürümlerde prompt dosyalarının başındaki `agent: 'agent'` satırı `mode: 'agent'` olarak yazılıyordu.
- Copilot seni tanımıyor gibi davranıyorsa: yanıttaki "References" kısmında `copilot-instructions.md` var mı bak.

## 5. Doküman nasıl verilir

- Dokümanı `docs/` klasörüne koy. Sayfa içeriğini kopyalayıp `docs/<kisa-ad>.md` olarak kaydedebilirsin. PDF ise metne çevir ya da bölüm bölüm sohbete yapıştır.
- Sonra `/oku docs/<kisa-ad>.md` yaz.

## 6. Her oturum

1. `/basla`
2. Çalış (`/oku`, `/kavram`, `/ders`)
3. `/bitir`

## 7. Güncelleme gelirse

Yeni zip'ten **sadece `.github/` klasörünü** eskisinin üzerine kopyala. `ILERLEME.md`, `KAVRAMLAR.md`, `dersler/` ve `docs/` dokunulmadan kalsın, yoksa hafıza silinir.
