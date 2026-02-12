# Prompts

Dieser Ordner enthält Prompt Templates, die im Rahmen des Projekts „Wahlhilfe GPT Landtagswahl BW26“ verwendet werden.

## Bildgenerierung: Visual Policy Translator

Datei: [`Bildgenerierung.txt`](Bildgenerierung.txt)

Ziel: Du lädst ein Referenzbild hoch und erzeugst daraus eine photorealistische, plausible ummodellierte Version.
Der Prompt ist so gestaltet, dass er neutral bleibt, keine Partei bewertet und das Ergebnis als umgestaltete Version des Referenzbildes erkennbar bleibt.

### Beispiel Output

Beispiel für eine Übersicht über mehrere Parteien bei identischer Perspektive und identischem Referenzbild:

![Wahlprogramme AI Übersicht](../Bilder/Wahlprogramme_AI.jpg)

### Benötigte Dateien

1. Referenzbild, zum Beispiel: [`../Bilder/Stuttgart_referenz.png`](../Bilder/Stuttgart_referenz.png)
2. Prompt Template: [`Bildgenerierung.txt`](Bildgenerierung.txt)

### Workflow: So nutzt du `Bildgenerierung.txt`

1. Öffne die Datei `Bildgenerierung.txt`.

2. Setze die Platzhalter per Suchen und Ersetzen
   1. Ersetze `{HIER PARTEI EINFÜGEN}` durch den Parteinamen, zum Beispiel `CDU`
   2. Ersetze `{PARTEI}` durch denselben Parteinamen
   3. Optional, aber empfohlen
      1. Setze `{INTENSITÄT}` auf `LOW`, `MED` oder `HIGH`
      2. Setze `{ZEITHORIZONT}` zum Beispiel auf `5 bis 10 Jahre`

   Hinweis: Der Prompt nutzt „(Partei)“ als interne Referenz auf die oben eingesetzte Partei. Das musst du normalerweise nicht zusätzlich ersetzen.

3. In ChatGPT
   1. Lade das Referenzbild als Attachment hoch, zum Beispiel `../Bilder/Stuttgart_referenz.png`
   2. Füge den angepassten Prompt vollständig ein
   3. Generiere das Bild

4. Ergebnisse speichern, Empfehlung
   1. Lege die generierten Bilder im Ordner `Bilder/` ab
   2. Benenne sie eindeutig, zum Beispiel
      1. `Stuttgart_CDU_MED.png`
      2. `Stuttgart_SPD_LOW.png`
      3. `Stuttgart_FDP_HIGH.png`

Hinweis: Wenn dein Bild bereits ein Copyright oder Watermark enthält, bleibt es beim Speichern unverändert erhalten.

### Workflow: „Alle Parteien“ Übersicht erzeugen

Wenn du eine Übersicht wie im Beispielbild erstellen willst, gehst du pro Partei identisch vor und änderst nur den Parteinamen im Prompt.

Parteien, die im Projektkontext typischerweise verwendet werden:
1. Die Basis
2. Die Linke
3. AfD
4. Freie Wähler
5. FDP
6. SPD
7. Bündnis Sahra Wagenknecht (BSW)
8. CDU
9. Bündnis 90 Die Grünen

Empfehlung für reproduzierbare Ergebnisse:
1. Nutze immer dasselbe Referenzbild
2. Halte Perspektive und Anker Regeln konstant
3. Verwende ein einheitliches Namensschema für Outputs, zum Beispiel `Stuttgart_<PARTEI>_<INTENSITÄT>.png`
4. Erstelle anschließend eine Collage oder ein Grid aus den Einzelbildern, falls gewünscht

## Lizenzhinweis

- Prompts und Text Inhalte sind für Forschung und Bildung frei nutzbar, mit Namensnennung.
- Kommerzielle Nutzung erfordert eine separate schriftliche Lizenz.

Siehe im Repository:
- `LICENSE-CONTENT-RESEARCH.md`
- `LICENSE-CONTENT-COMMERCIAL.md`
- `TRADEMARK.md`

## Wichtige Hinweise

Dieses Tool ersetzt keine Wahlentscheidung, sondern hilft dabei, Wahlprogramme besser zu verstehen.

Die hier genannten Standpunkte sind unbedingt in den Original Wahlprogrammen zu überprüfen:
https://www.landtagswahl-bw.de/wahlprogramme-2026

Diese Wahlprogrammanalyse ist kein offizielles Angebot einer Behörde, Partei oder Redaktion und keine Wahlberatung. Sie soll dabei helfen, Wahlprogramme zu strukturieren und besser zu verstehen.
