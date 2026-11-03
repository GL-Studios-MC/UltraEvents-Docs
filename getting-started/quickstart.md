# Installation & Quickstart

Getting UltraEvents up and running on your server takes less than 2 minutes.

---

### Requirements

* **Minecraft Version**: 1.20, 1.21, 26.1, 26.2, 26.3 (`Mounts of Mayhem`) and above.
* **Server Software**: Paper, Purpur, Spigot, or Folia.
* **Java Version**: Java 21+.
* **Optional Plugins**:
  * [Vault](https://www.spigotmc.org/resources/vault.34315/) + Economy plugin (for money rewards).
  * [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) (for scoreboards/tablists).
  * [WorldEdit](https://enginehub.org/worldedit/) (optional, for region handling).

---

### 1. Installation

1. Download **UltraEvents PRO** or [Download UltraEvents Lite on SpigotMC](https://www.spigotmc.org/resources/ultraevents-lite-automated-mini-game-events-system-1-20-26-3.140244/).
2. Place the JAR file into your server's `plugins/` directory.
3. Restart or start your server (do not use `/reload`).
4. UltraEvents will automatically generate its configuration files and default arena world templates.

---

### 2. First-Time Setup (60 Seconds)

1. Join your server with Operator (`op`) permissions.
2. Type `/eventadmin setup wand` to receive the visual setup tool.
3. Select your arena floor corners with Left-Click (Pos 1) and Right-Click (Pos 2).
4. Run:
   ```bash
   /eventadmin setup lobby      # Sets player spawn location
   /eventadmin setup spectator  # Sets spectator viewing platform
   /eventadmin setup exit       # Sets where players return after event
   /eventadmin setup save       # Verifies and saves everything
   ```
5. You are ready! Start your first event with `/eventadmin` -> Click **Event Starten**.
