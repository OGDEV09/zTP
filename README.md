# zTP - Teleportation Plugin

Ein erweitertes Teleportations-Plugin mit GUI-Menü, Cooldowns und Anti-Spam-Schutz.

## 📥 Installation

1. Download the latest version
2. Place the `.jar` file in your `plugins/` folder
3. Restart your server

## 📋 Features

- ✅ GUI-based teleport requests
- ⏱️ Configurable cooldowns (10min default)
- 🔒 Permission system
- 🔊 Customizable sounds
- 📝 Fully configurable messages
- 🛡️ Anti-spam protection

## 🛠️ Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `/tpaall` | Send TP request to all players | `tpall.use` |
| `/tpaallaccept` | Open accept menu | `tpall.accept` |
| `/ztpreload` | Reload configuration | `ztp.reload` |

## 🔧 Configuration

`config.yml` is auto-generated. Default values:

```yaml
# ====================================================
# zTP - Teleportationssystem Konfiguration
# ====================================================

settings:
  # Teleport-Einstellungen
  request-lifetime-seconds: 60  # Wie lange Anfragen gültig bleiben (in Sekunden)
  teleport-sound: "ENTITY_ENDERMAN_TELEPORT"  # Sound bei Teleportation
  teleport-countdown: 5  # Countdown-Dauer vor Teleport (in Sekunden)
  tpall-cooldown-seconds: 600  # Cooldown für /tpaall Befehl (in Sekunden) - 10 Minuten
  movement-cancellation: true  # Ob Bewegung den Teleport abbricht
  allow-multiple-requests: false  # Mehrere parallele Anfragen erlauben

  # GUI-Einstellungen
  gui-size: 27  # Größe des Inventars (9, 18, 27, etc.)
  gui-accept-item: "LIME_STAINED_GLASS_PANE"  # Material für Annehmen-Button
  gui-deny-item: "RED_STAINED_GLASS_PANE"  # Material für Ablehnen-Button

  # Sound-Einstellungen
  notification-sound: "BLOCK_NOTE_BLOCK_PLING"  # Sound bei neuer Anfrage
  sound-volume: 1.0  # Lautstärke (0.1 - 1.0)
  sound-pitch: 1.0  # Tonhöhe (0.5 - 2.0)

messages:
  # Systemnachrichten
  expired_notify: "&cDie Teleport-Anfrage ist abgelaufen."
  reload-success: "&aKonfiguration erfolgreich neu geladen!"
  reload-fail: "&cFehler beim Neuladen der Konfiguration!"

  # Fehlermeldungen
  errors:
    no-request: "&cDu hast keine aktive Teleport-Anfrage."
    cooldown: "&cDu kannst &e/tpaall &cerst in &e{seconds} Sekunden &cwieder benutzen."
    already-interacted: "&cDu kannst erst in {time} Sekunden wieder auf eine Anfrage reagieren."
    no-permission: "&cDazu hast du keine Berechtigung!"
    player-offline: "&cDer Spieler ist offline."
    movement-canceled: "&cTeleportation abgebrochen wegen Bewegung!"

  # Teleport-Nachrichten
  teleport:
    countdown: "&7Teleportation in &6{seconds} &7Sekunden..."
    success: "&aDu wurdest zu &e{player} &ateleportiert!"
    canceled: "&cTeleportation abgebrochen!"
    deny: "&cDu hast die Teleport-Anfrage abgelehnt."
    actionbar: "&bTeleportation in &e{seconds}&b Sekunden..."

  # Anfrage-Nachrichten
  request:
    line1: "&6{player} &7möchte, dass alle Spieler zu ihm kommen!"
    line2: "&a&l[KLICKE HIER] &7um die Anfrage anzunehmen"
    sent: "&aTeleport-Anfrage an &e{count} &aSpieler gesendet!"

  # GUI-Einstellungen
  gui:
    title: "&8TP ALL ANFRAGE"
    accept: "&a✔ Annehmen"
    deny: "&c✖ Ablehnen"
    head_name: "&eTeleport zu &6{player}"
    lore:
      - "&7Klicke zum Annehmen"
      - "&7oder schließe das Inventar"
      - "&7zum Ablehnen"

# Fortgeschrittene Einstellungen
advanced:
  # Schutz vor Missbrauch
  max-requests-per-minute: 5  # Maximale Anfragen pro Minute
  spam-protection: true  # Anti-Spam Schutz

  # Logging-Einstellungen
  log-teleports: true  # Teleportationen protokollieren
  log-format: "[zTP] {player} teleportierte zu {target}"
