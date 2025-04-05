zTP - Teleportation Plugin
GitHub
Spigot Version

Ein erweitertes Teleportations-Plugin mit GUI-Menü, Cooldowns und Anti-Spam-Schutz.

📥 Installation
Lade die neueste Version herunter

Platziere die .jar-Datei in deinem plugins/-Ordner

Starte deinen Server neu

📋 Features
✅ GUI-basierte Teleportationsanfragen

⏱️ Konfigurierbare Cooldowns (10 Minuten Standard)

🔒 Permissions-System

🔊 Anpassbare Sounds

📝 Vollständig konfigurierbare Nachrichten

🛡️ Anti-Spam-Schutz

🛠️ Kommandos
Befehl	Beschreibung	Permission
/tpaall	Sendet eine TP-Anfrage an alle Spieler	tpall.use
/tpaallaccept	Öffnet das Annahme-Menü	tpall.accept
/ztpreload	Lädt die Konfiguration neu	ztp.reload
🔧 Konfiguration
Die config.yml wird automatisch generiert. Hier die Standardwerte:

yaml
Copy
settings:
  teleport-countdown: 5
  tpall-cooldown-seconds: 600
  gui-accept-item: "LIME_STAINED_GLASS_PANE"
  gui-deny-item: "RED_STAINED_GLASS_PANE"

messages:
  gui:
    title: "&8Teleport-Anfrage von {player}"
    accept: "&a✔ Annehmen"
    deny: "&c✖ Ablehnen"
📜 Permissions
yaml
Copy
permissions:
  tpall.use:
    description: Erlaubt /tpaall
    default: op
  tpall.accept:
    description: Erlaubt Anfragen anzunehmen
    default: true
  ztp.reload:
    description: Erlaubt Konfig-Neuladen
    default: op
📦 Abhängigkeiten
Spigot/Paper 1.16+
Java 11+
