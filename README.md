# Diplomarbeit Template TGM

Ein vollständiges LaTeX-Template für Diplomarbeiten am TGM in der Abteilung HBG.

## 📁 Projektstruktur

```
Diplomarbeit_Template_TGM/
├── main.tex                    # Hauptdatei des LaTeX-Dokuments
├── frontmatter/               # Vorspann-Dateien
│   ├── titelseite.tex        # Titelseite
│   ├── eidesstattliche_erklaerung.tex
│   ├── kurzfassung.tex       # Deutsche Zusammenfassung
│   ├── abstract.tex          # Englische Zusammenfassung
│   └── einleitung.tex        # Einleitung
├── mainmatter/               # Hauptkapitel (hier fügst du deine Inhalte ein)
├── backmatter/               # Schlussteil
│   ├── zusammenfassung.tex   # Fazit/Zusammenfassung
│   └── literatur.bib         # Bibliografie-Datei
└── bilder/                   # Ordner für Abbildungen und Grafiken
```

## 🚀 Quick Start

1. **Template klonen oder herunterladen**
2. **Anpassen der persönlichen Daten** in den entsprechenden Dateien:
   - `frontmatter/titelseite.tex` - Titel, Name, Betreuer, etc.
   - `main.tex` Zeile 58-60 - PDF-Metadaten
3. **Deine Kapitel hinzufügen**:
   - Erstelle `.tex` Dateien im `mainmatter/` Ordner (z.B. `kapitel1.tex`, `kapitel2.tex`)
   - Füge sie in `main.tex` im Mainmatter-Bereich mit `\input{mainmatter/kapitel1}` ein
4. **Literatur ergänzen** in `backmatter/literatur.bib`
5. **Kompilieren** mit pdflatex + biber

## 📋 Erforderliche Software & Pakete

### LaTeX-Distribution
- **TeX Live** (empfohlen) oder **MiKTeX**
- **pdflatex** für die Kompilierung
- **biber** für Literaturverzeichnis

### Wichtige LaTeX-Pakete
Das Template verwendet folgende Pakete (meist in Standard-Distributionen enthalten):

**Grundpakete:**
- `babel` (ngerman)
- `inputenc`, `fontenc`
- `geometry`, `setspace`
- `graphicx`, `float`

**Erweiterte Features:**
- `biblatex` mit Backend `biber` - **Literaturverzeichnis**
- `glossaries` - Glossar und Abkürzungen
- `hyperref` - PDF-Links und Metadaten
- `listings`, `xcolor` - Code-Syntax-Highlighting
- `fancyhdr` - Kopf-/Fußzeilen
- `booktabs` - Professionelle Tabellen
- `csquotes` - Korrekte Anführungszeichen

## ⚠️ Wichtige Hinweise

### PDF-Dateien in Git
- **PDFs sind standardmäßig ignoriert** (siehe `.gitignore` Zeile 22: `*.pdf`)
- **Grund:** PDF-Dateien sind groß und ändern sich bei jeder Kompilierung
- **Wenn du PDFs tracken möchtest:** Entferne `*.pdf` aus der `.gitignore`

### Literaturverzeichnis
- Verwendet **biber**
- Bibliografie-Einträge kommen in `backmatter/literatur.bib`
- Stil: numerisch (`style=numeric`)

### Abbildungen
- Speichere Bilder im `bilder/` Ordner
- Unterstützte Formate: PDF, PNG, JPG
- Verwendung: `\includegraphics{bilder/meinbild.png}`

## 🎨 Anpassungen

### Schriftart ändern
```latex
\usepackage{times}      % Times New Roman
\usepackage{lmodern}    % Latin Modern (Standard)
```

### Zeilenabstand
```latex
\singlespacing          % 1-fach
\onehalfspacing        % 1.5-fach (Standard)
\doublespacing         % 2-fach
```

### Seitenränder
Aktuell: links 3cm, rechts 2cm, oben/unten 2.5cm
```latex
\usepackage[left=3cm,right=2cm,top=2.5cm,bottom=2.5cm]{geometry}
```

## 📚 Verwendete Standards

- **Dokumentklasse:** report (einseitig, 12pt, A4)
- **Sprache:** Deutsch (ngerman)
- **Kodierung:** UTF-8
- **Zitationsstil:** Numerisch
- **Seitennummerierung:** Arabische Zahlen durchgehend

## 🆘 Häufige Probleme

### "Package biblatex Error: Please (re)run Biber"
- **Lösung:** `biber main` ausführen, dann erneut `pdflatex main.tex`

### Umlaute werden nicht korrekt dargestellt
- **Lösung:** Datei in UTF-8 kodiert speichern und `\usepackage[utf8]{inputenc}` verwenden

### Bilder werden nicht gefunden
- **Lösung:** Pfad relativ zur `main.tex` angeben: `\includegraphics{bilder/meinbild.png}`

## 🤝 Beitragen

Dieses Template ist für TGM-Schüler*innen gedacht. Verbesserungsvorschläge und Issues sind willkommen!


**Viel Erfolg bei deiner Diplomarbeit! 🎓**