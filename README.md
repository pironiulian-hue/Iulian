# Transcriere Ședințe

Aplicație web simplă pentru transcrierea live a ședințelor, direct în browser. Nu necesită instalare, server sau cont.

## Cum o folosești

1. Deschide `index.html` în **Google Chrome** sau **Microsoft Edge** (recunoașterea vocală funcționează doar în aceste browsere).
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

- Recunoașterea vocală a Chrome/Edge trimite audio către serviciul de recunoaștere al browserului (Google/Microsoft) — nu folosi pentru discuții confidențiale dacă asta e o problemă.
- Vorbitorii nu sunt detectați automat; se selectează manual.
- Datele rămân doar în browserul în care au fost create. Exportă transcrierile importante.
