# Residenz-Life – Setup für mehrere Launcher

Residenz-Life nutzt `packwiz` mit Auto-Update vor dem Spielstart.

## Downloads

Im GitHub-Release `latest` findest du:

- `packwiz-installer-bootstrap.jar` (empfohlen für Auto-Update)
- `Residenz-Life-<VERSION>-curseforge.zip` (CurseForge-Export)
- `Residenz-Life-<VERSION>.mrpack` (Modrinth-Export)

## Einheitlicher Update-Befehl

Diesen Befehl nutzt du überall dort, wo der Launcher einen Pre-Launch-/Custom-Command erlaubt:

`java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`

## Voraussetzungen

- Java 21 installiert
- Minecraft `1.21.8`
- Fabric Loader `0.17.3`
- `packwiz-installer-bootstrap.jar` im Instanzordner

## Prism Launcher / MultiMC (empfohlen)

1. Neue Instanz mit Minecraft `1.21.8` und Fabric `0.17.3` erstellen.
2. `packwiz-installer-bootstrap.jar` in den Instanzordner kopieren.
3. Instanz-Einstellungen öffnen und den Pre-Launch-Command setzen.
4. Folgenden Command eintragen:
   - `java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`
5. Spiel starten. Updates werden bei jedem Start automatisch ausgeführt.

## Modrinth App (gut geeignet)

1. Neue Fabric-Instanz (`1.21.8`) erstellen.
2. `packwiz-installer-bootstrap.jar` in den Instanzordner kopieren.
3. In den Instanz-Einstellungen den Custom-/Pre-Launch-Command setzen.
4. Diesen Command eintragen:
   - `java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`
5. Starten und automatisch vor jedem Launch aktualisieren lassen.

## ATLauncher (möglich)

1. Neue Fabric-Instanz für `1.21.8` erstellen.
2. `packwiz-installer-bootstrap.jar` in den Instanzordner legen.
3. Pre-Launch-Command in den Instanz-Einstellungen definieren.
4. Diesen Command verwenden:
   - `java -jar packwiz-installer-bootstrap.jar https://raw.githubusercontent.com/Flumuffel/Residenz-Life/main/pack.toml`
5. Beim Start lädt der Installer Updates automatisch.

## CurseForge (nur manuell, nicht empfohlen)

CurseForge bietet für dieses Setup keinen verlässlichen Pre-Launch-Command an.  
Dadurch ist **kein echtes Auto-Update bei jedem Start** möglich.

Wenn du CurseForge trotzdem nutzen willst:

1. Lade `Residenz-Life-<VERSION>-curseforge.zip` aus dem Release herunter.
2. Importiere die ZIP in CurseForge.
3. Für Updates musst du neue Export-ZIPs manuell erneut importieren oder die Modliste manuell nachziehen.

Für automatische Updates ist Prism/MultiMC oder Modrinth App klar besser geeignet.

## Troubleshooting

- **Java nicht gefunden**: Prüfe `java -version` in der Konsole.
- **Datei fehlt**: Prüfe, ob `packwiz-installer-bootstrap.jar` im Instanzordner liegt.
- **Update schlägt fehl**: URL testen, Firewall/Proxy prüfen.
- **Schreibrechte fehlen**: Launcher normal starten und Rechte im Instanzordner prüfen.
