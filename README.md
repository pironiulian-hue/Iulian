# Transcriere Ședințe

Aplicație web simplă pentru transcrierea live a ședințelor, direct în browser. Nu necesită instalare, server sau cont.

## Instalare pe iPhone / iPad

Aplicația e o *aplicație web instalabilă* (PWA): după instalare are icon pe ecranul principal, se deschide pe tot ecranul și pornește și fără internet.

1. Publică aplicația pe un link HTTPS (microfonul nu funcționează altfel). Cel mai simplu, cu **GitHub Pages**:
   GitHub → repository → **Settings → Pages** → *Source: Deploy from a branch* → alege ramura și folderul `/ (root)` → **Save**.
   După 1–2 minute primești un link de forma `https://<utilizator>.github.io/<repository>/`.
   (Pentru un repository privat, GitHub Pages cere un plan plătit; altfel poți folosi gratuit Netlify sau Cloudflare Pages.)
2. Pe iPhone, deschide linkul în **Safari**.
3. Apasă butonul **Partajează** (pătratul cu săgeată) → **Adaugă pe ecranul principal** → **Adaugă**.
4. Prima dată când apeși **▶ Începe**, permite accesul la microfon și la recunoașterea vocală.

Setări necesare pe iPhone:
- **Configurări → General → Tastatură → Activează dictarea** (recunoașterea vocală a Safari folosește dictarea iOS).
- Dacă ai refuzat microfonul: **Configurări → Safari → Microfon → Permite**.

Sfaturi pentru iPhone:
- Ține aplicația deschisă și în prim-plan în timpul ședinței. Aplicația ține ecranul aprins (iOS 16.4+); dacă ieși din ea, transcrierea se oprește și repornește automat când revii.
- Înregistrarea audio simultană e oprită implicit pe iPhone, pentru că poate bloca transcrierea.
- Atinge numele celui care vorbește ca să-l selectezi; atinge-l din nou ca să-l redenumești sau să-l elimini.

## Cum o folosești

1. Deschide aplicația în **Safari** (iPhone/iPad), **Google Chrome** sau **Microsoft Edge** (Firefox nu are recunoaștere vocală).
   - Pentru cea mai bună compatibilitate cu microfonul, servește fișierul local: `python3 -m http.server` și deschide `http://localhost:8000`.
2. Completează titlul, alege limba (implicit română) și adaugă participanții.
3. Apasă **▶ Începe** și permite accesul la microfon.
4. În timpul ședinței, selectează cine vorbește (click pe nume sau tastele **1–9**). **Spațiu** = pauză/continuare.
5. La final apasă **⏹ Încheie**, apoi exportă.

## Funcționalități

- Transcriere live cu marcaj de timp, în română și alte limbi
- Etichetare vorbitori (redenumire cu dublu-click, schimbare vorbitor pe rând cu click pe nume)
- Editare directă a oricărui rând (click pe text)
- Marcare rânduri ca ✅ **Decizie** sau 📌 **Acțiune**
- **Minută** generată automat: decizii, acțiuni, intervenții pe participant, notițe
- Căutare în transcriere
- Înregistrare audio în paralel, descărcabilă
- Export: `.txt`, `.md`, Word (`.doc`), subtitrare `.srt`, `.json`; copiere în clipboard
- Istoric ședințe salvat automat în browser (localStorage)

## Limitări

- Recunoașterea vocală trimite de regulă audio către serviciul browserului (Apple, Google sau Microsoft) — nu folosi pentru discuții confidențiale dacă asta e o problemă.
- Vorbitorii nu sunt detectați automat; se selectează manual.
- Datele rămân doar în browserul în care au fost create. Exportă transcrierile importante.
