
---

## 2️⃣ Pull-Request-Template (für `.github/pull_request_template.md`)

Lege im Repo den Ordner `.github` an und darin die Datei `pull_request_template.md`:

```markdown
## 📝 Beschreibung

_Beschreibe kurz, was dieser Pull Request tut._
- [ ] Feature
- [ ] Bugfix
- [ ] Refactoring
- [ ] Dokumentation

**Issue-Referenz:** Closes #<issue-nummer>

---

## ✅ Änderungen

_Kurze Liste der wichtigsten Änderungen:_
- ...
- ...
- ...

---

## 🔍 Motivation & Kontext

_Warum ist diese Änderung nötig? (z. B. User Story, Fehlerbeschreibung, fachlicher Hintergrund)_  
- ...

---

## 🧪 Tests

_Beschreibe, welche Tests durchgeführt wurden:_

- [ ] Unit-Tests
- [ ] Integrationstests
- [ ] Manuelle Tests im Browser
- [ ] Sonstige: …

**Details:**
- `npm test` / `dotnet test` / …  
- Manuelle Testfälle (z. B. „Antrag erstellen und Status prüfen“)

---

## 💣 Breaking Changes

_Gibt es Änderungen, die bestehende Funktionalität brechen könnten?_

- [ ] Ja
- [ ] Nein

**Wenn ja, welche?**
- ...

---

## 📸 Screenshots (optional)

_Falls UI-Änderungen vorgenommen wurden, Screenshots einfügen:_

- Vorher:
- Nachher:

---

## ✅ Checkliste Autor:in

_Bitte vor dem Request eines Reviews prüfen:_

- [ ] Code kompiliert lokal
- [ ] Relevante Tests geschrieben/aktualisiert
- [ ] Alle Tests lokal erfolgreich
- [ ] Branch ist auf dem aktuellen Stand von `main`
- [ ] PR ist klein genug und sinnvoll geschnitten
- [ ] Fachliche Akzeptanzkriterien der Story sind erfüllt

---

## 👀 Checkliste Reviewer:in

- [ ] Funktionalität entspricht dem Issue / der Beschreibung
- [ ] Code ist verständlich und wartbar
- [ ] Keine offensichtlichen Duplication / „Code Smells“
- [ ] Tests sind sinnvoll und ausreichend
- [ ] Architektur-/Schichtenmodell wird respektiert
- [ ] CI ist grün
