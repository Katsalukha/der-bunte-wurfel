# 🎲 Der bunte Würfel

Eine digitale Umsetzung des DDR-Kinderspiels **„Der bunte Würfel“**
(VEB Plasticart Annaberg-Buchholz, Ag 742-19-83). Spiele direkt im Browser
gegen **1–3 Bots** – die Würfe sind zufällig (für dich und die Bots).

👉 **Spielen:** `https://katsalukha.github.io/der-bunte-wurfel`

---

## Spielen

1. Wähle die Anzahl der Bot-Gegner (1–3).
2. Du spielst **Rot**. Drücke **„Würfeln“**.
3. Bring deine 4 Figuren ins farbige Haus – nicht als Letzter!

## Originalregeln (VEB Plasticart)

Ein Würfelspiel für Vorschulkinder ab dem 4. Lebensjahr. Würfel und Spielfeld
tragen **6 Bilder**: 🌸 Blume · 🍄 Pilz · ⚽ Ball · 🐌 Schnecke · ⭐ Stern · 🦋 Schmetterling.

- **Bewegung – kein Zählen!** Du würfelst ein Symbol und ziehst deine Figur
  **vorwärts bis zum nächsten Feld, das genau dieses Symbol zeigt**.
- **🌸 Blume = Wahl + Extra-Wurf:** Du wählst – eine neue Figur einsetzen
  *oder* eine Figur auf dem Brett zum nächsten 🌸-Feld ziehen. Danach darfst
  du **noch einmal würfeln**; bei erneuter Blume geht es weiter, bis ein
  anderes Symbol kommt.
- **Nur 1 Figur pro Feld:** Steht auf dem Zielfeld schon eine *eigene* Figur,
  darf dort keine zweite hin – du musst eine andere Figur ziehen. Steht dort
  eine *fremde* Figur, wird sie geschlagen und muss neu eingesetzt werden.
- **Kein Überspringen:** Liegt auf dem Weg zum Zielfeld *irgendeine* Figur –
  auch eine *eigene* – ist dieser Zug nicht möglich. Aus „Staus“ kommst du nur
  heraus, indem du genau das Symbol würfelst, auf dem eine *gegnerische* Figur
  steht, und sie schlägst. Eigene Figuren clever verteilen!
- **Haus & Ziel:** Nach einer vollen Runde wartet die Figur am **Tor** des
  eigenen Hauses (ein Ringfeld – *nicht sicher*, kann geschlagen werden). Das
  Haus ist ein **Korridor aus 4 Symbol-Feldern**; würfle das Symbol eines
  Korridor-Feldes, um hineinzuziehen. Figuren im Haus dürfen **weiter nach
  vorn rücken** (Symbol eines tieferen Feldes) – auch hier gilt **kein
  Überspringen**, so bleibt der Eingang frei. Wer alle 4 im Haus hat, ist
  fertig – gespielt wird, bis nur einer übrig ist: der **Verlierer**.

> **Umsetzung:** Diese Fassung folgt der *erweiterten Spielregel für ältere
> Kinder* (4 Figuren je Farbe) inkl. der Experten-Schlagen-Regel. Die
> *einfache Original-Regel* hat nur 1 Figur je Kind und kein Schlagen.
> Quelle: Originalanleitung VEB Plasticart Annaberg-Buchholz.

## Auf GitHub Pages veröffentlichen

1. Erstelle ein **öffentliches** Repository mit dem Namen `der-bunte-wurfel`.
2. Lade in den Repo-Hauptordner:
   - `index.html` **(erforderlich)**
   - `board.jpg` **(erforderlich** – das Originalbrett-Foto, auf dem gespielt wird)
   - optional `README.md` und `calibrate.html` (Werkzeug zum Neu-Einmessen des Bretts)
3. Im Repo: **Settings → Pages → Build and deployment**
   → *Source:* **Deploy from a branch**
   → *Branch:* **main** / Ordner **/(root)** → **Save**.
4. Nach ein paar Minuten erreichbar unter:
   `https://katsalukha.github.io/der-bunte-wurfel`

Keine Build-Schritte, keine Abhängigkeiten – reines HTML/CSS/JS.

## Technik

- `index.html` (kein Build, keine externen Libraries) + `board.jpg`.
- Gespielt wird auf dem fotografierten Originalbrett; Felder, Startfelder und
  Endpunkte wurden mit `calibrate.html` aus dem Foto eingemessen (Pixel-Maske).
- Spiellogik, Bot-KI und Rendering in Vanilla-JavaScript.
- Funktioniert offline und auf Mobilgeräten.
