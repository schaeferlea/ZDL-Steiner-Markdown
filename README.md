# ZDL-Steiner-Format mit R Markdown
Eine Pandoc-Lösung um von R Markdown ins Steiner-Format (docx) zu konvertieren. Das hier ist ein erster Lösungsversuch. Überarbeitungen sind willkommen!

## Verwendung

1. Pandoc installieren (vgl. https://pandoc.org)
2. Zusatzfilter für Referenzen [pandoc-crossref](https://github.com/lierdakil/pandoc-crossref) installieren.
2. Terminal-Befehl: pandoc -f markdown -t docx --reference-doc=steiner.dotm --resource-path=.:figures  --filter pandoc-crossref --filter pandoc-citeproc --bibliography=sample.bib -o output.docx doc.rmarkdown
3. Spaß haben mit Rmarkdown

## Noch nicht ideal
Händisch muss noch nachbearbeitet werden:

* Grafiken float-Umgebung
* Refrenzen zu glossierten Beispielen funktioniert über den Filter pangloss nur bei PDF und HTML Export
* Unschöne Lösung für Kapitälchen: Autornamen mit \textsc{} in der .bib-Datei auszeichnen



