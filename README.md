# Residenz-Life - Multi-Launcher Setup mit Auto-Update

Dieses Repo verteilt den Installer als `packwiz-installer-bootstrap.jar`.
Der gleiche Command wird in allen Launchern verwendet:

`java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`

## Voraussetzungen

- Java 21 installiert
- Minecraft `1.21.8`
- Fabric Loader `0.17.3`
- Die Datei `packwiz-installer-bootstrap.jar` aus den GitHub Releases

## Prism Launcher / MultiMC

1. Neue Instanz erstellen:
   - Minecraft `1.21.8`
   - Mod Loader: Fabric `0.17.3`
2. `packwiz-installer-bootstrap.jar` in den Instanzordner kopieren.
3. Instanz bearbeiten -> Einstellungen -> Befehl vor dem Start ausführen.
4. Als Pre-Launch-Command eintragen:
   - `java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`
5. Spiel starten. Vor jedem Start werden Updates automatisch geprüft und geladen.

## CurseForge App

1. Neues benutzerdefiniertes Fabric-Profil erstellen:
   - Minecraft `1.21.8`
   - Fabric `0.17.3`
2. Profilordner öffnen und `packwiz-installer-bootstrap.jar` hineinkopieren.
3. In den Profil-/Launch-Einstellungen ein Pre-Launch- oder Wrapper-Command hinterlegen:
   - `java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`
4. Danach normal starten. Das Update läuft bei jedem Start vor Minecraft.

Hinweis: Falls deine CurseForge-Version keinen direkten Pre-Launch-Command anbietet, starte die Instanz über ein kleines Startskript, das zuerst den obigen Java-Befehl ausführt und dann Minecraft startet.

## Modrinth App

1. Neue Fabric-Instanz erstellen:
   - Minecraft `1.21.8`
   - Fabric `0.17.3`
2. Instanzordner öffnen und `packwiz-installer-bootstrap.jar` hineinkopieren.
3. Unter Instanz-Einstellungen den Start/Pre-Launch-Command setzen:
   - `java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`
4. Instanz starten. Updates werden vor jedem Spielstart synchronisiert.

## ATLauncher

1. Neue Fabric-Instanz für Minecraft `1.21.8` erstellen.
2. `packwiz-installer-bootstrap.jar` in den Instanzordner legen.
3. In den Instanz-Einstellungen einen Pre-Launch-Command definieren:
   - `java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`
4. Beim Start der Instanz werden Updates automatisch geladen.

## Troubleshooting

- **Java nicht gefunden**: Prüfe, ob `java -version` in der Konsole funktioniert.
- **Datei nicht gefunden**: Stelle sicher, dass `packwiz-installer-bootstrap.jar` im Instanzordner liegt.
- **Keine Updates / Netzwerkfehler**: Teste die URL im Browser und prüfe Firewall/Proxy.
- **Berechtigungsprobleme**: Launcher mit normalen Benutzerrechten starten und Schreibrechte im Instanzordner prüfen.
