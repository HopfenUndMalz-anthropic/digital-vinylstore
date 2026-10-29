# Virtueller Plattenstore

Statische Website (eine HTML-Datei, keine Abhängigkeiten). Genres per Reiter, pro Genre Top 10 mit Preisspanne und Shop-Link.

## Hosting über GitHub Pages
1. Neues Repository auf GitHub anlegen (z. B. `plattenstore`).
2. Diesen Ordner hochladen: `git init && git add . && git commit -m "Init" && git branch -M main && git remote add origin <URL> && git push -u origin main`
3. Im Repo: Settings → Pages → Source: `Deploy from a branch`, Branch `main`, Ordner `/ (root)`.
4. Die Seite ist danach unter `https://<dein-user>.github.io/plattenstore/` erreichbar.

## Bekannte Einschränkungen
- **Produktlinks:** Der Shop lädt Produktlisten per JavaScript. Die Produkt-URLs sind daher nicht verifiziert. Der Button „Im Shop suchen“ nutzt den Parameter `?s=`, der nicht getestet ist. Vor dem Veröffentlichen bitte einmal klicken und prüfen.
- **Genre-Links:** Nur `rock-vinyl-LP` ist bestätigt. Die übrigen Slugs sind Annahmen nach demselben Muster.
- **Preise:** Alle Preisspannen sind Schätzungen, keine Live-Preise.
- **Top-10-Auswahl:** Die Listen stammen aus Modellwissen und sind nicht gegen aktuelle Charts oder Kritiker-Bestenlisten geprüft. Die Kennzeichnung „Aktuell“ ist nicht verifiziert.
- **Aktualisierung:** Noch nicht eingerichtet. Geplant ist ein wiederkehrender Task (täglich oder wöchentlich), der die Listen per Websuche aktualisiert.

## Daten ändern
Die Platten stehen als Array `GENRES` in `index.html`. Ein Eintrag hat `artist`, `title`, `year`, `source`, `reason` und `price`.
