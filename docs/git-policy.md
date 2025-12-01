# Git- und Branching-Policy

Dieses Dokument beschreibt den gemeinsamen Umgang mit Git, Branches, Commits und Pull Requests
im SWE-III-Projekt „Digitaler Workflow Abschlussarbeiten“.

## 1. Ziele

- Stabile `main`-Branch (immer build- und testbar)
- Transparenter Workflow für alle Teammitglieder
- Nachvollziehbare Historie (Commits, PRs, Reviews)
- Automatisierte Qualitätssicherung (CI: Build, Tests, Lint)

---

## 2. Branch-Struktur

Wir verwenden eine vereinfachte Form von GitHub Flow mit optionalen Release-Branches.

### 2.1 Haupt-Branch

- **`main`**
  - Immer in *deploybarem* Zustand (Build & Tests grün)
  - Nur Änderungen über Pull Requests (keine direkten Commits)
  - Von GitHub als „protected branch“ konfiguriert:
    - mindestens 1 Review
    - CI muss erfolgreich sein

### 2.2 Kurzlebige Feature-Branches

- **Namenskonvention**:
  - `feature/<issue-nummer>-<kurze-beschreibung>`
  - Beispiele:
    - `feature/12-projektantrag-anlegen`
    - `feature/7-statusuebersicht-student`
- Zweck:
  - Neue Features / User Story / Refactorings

### 2.3 Bugfix-Branches

- **Namenskonvention**:
  - `bugfix/<issue-nummer>-<kurze-beschreibung>`
  - Beispiele:
    - `bugfix/21-falscher-status-im-dashboard`
- Wird genauso behandelt wie Feature-Branches.

### 2.4 Optionale Release-Branches

- Bei wichtigen Meilensteinen (z. B. Präsentation, Abgabe) nutzen wir:
  - `release/<version>`
  - Beispiel: `release/1.0`
- In diesem Branch:
  - nur noch Bugfixes
  - keine neuen Features
- Nach der Abgabe:
  - Bugfixes ggf. zurück nach `main` mergen

---

## 3. Workflow

### 3.1 Neues Issue → Branch

1. Issue im GitHub-Board erstellen oder auswählen.
2. Branch aus `main` erstellen:
   ```bash
   git checkout main
   git pull
   git checkout -b feature/<issue-nr>-<beschreibung>
