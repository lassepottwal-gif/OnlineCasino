[README.txt](https://github.com/user-attachments/files/34443815/README.txt)
PUNKTspiel / NEON PALACE – aktualisierte Versionen

Dateien:
- Punktspiel.html: Wettseite mit korrigierten Meilenstein-Checkpoints, anklickbaren Details und Account-Anmeldung.
- Neon_Palace.html: Neon Palace mit Texas Hold’em (2–8 Spieler), Small-/Big-Blinds, vier Setzrunden, Check/Call/Raise/Fold, Aufstehen vom Tisch, Start durch jeden sitzenden Spieler, GG-Animation, eigenem Sound-Upload und Solo-/abwechselndem Duellmodus bei Roulette, Blackjack und Slots.
- GGAnimation.gif: muss im selben Ordner wie Neon_Palace.html liegen, damit die Animation angezeigt wird.

Einrichtung:
1. Beide HTML-Dateien und GGAnimation.gif zusammen in denselben Ordner legen.
2. In Punktspiel und Neon Palace dieselbe Firebase Realtime Database URL und denselben Spielschlüssel verwenden.
3. In Punktspiel zuerst unter Einstellungen die Synchronisierung verbinden. Danach mit dem Neon-Palace-Account und dessen Passwort anmelden.
4. Custom-Sounds werden lokal im jeweiligen Browser gespeichert; auf einem anderen Gerät müssen sie erneut ausgewählt werden.
5. Roulette/Blackjack/Slots: „Duell – abwechselnd“ ist ein Hot-Seat-Modus auf demselben Gerät. Wählt einen zweiten Neon-Palace-Account; beide spielen mit ihrem eigenen virtuellen Chipkonto.

Wichtige technische Grenzen:
- Die Hold’em-Version unterstützt 2–8 Spieler und normale Setzrunden, aber keine All-ins oder Side Pots. Spieler müssen ihre Einsätze vollständig bezahlen können.
- Die Karten werden in Firebase gespeichert und in der Oberfläche verdeckt. Mit direktem Datenbank-Lesezugriff kann ein Mitspieler die Karten dennoch auslesen. Für wirklich private Karten und belastbare Zugriffskontrolle ist ein vertrauenswürdiger Backend-Dienst mit Firebase Authentication und restriktiven Datenbankregeln nötig.
- Der Passwortschutz der Wettseite verwendet denselben SHA-256-Passworthash wie Neon Palace. Die Sicherheit hängt zusätzlich von den Firebase-Datenbankregeln ab.

Alle Einsätze sind ausschließlich virtuelle Chips/Punkte ohne Geldwert.
