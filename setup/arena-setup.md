# In-Game Setup Wizard

With UltraEvents, you don't need to manually write coordinates into YAML files. The entire arena setup can be completed in-game in less than 60 seconds.

---

### Step-by-Step Setup Tutorial

#### 1. Obtain the Setup Wand
Run the command:
```bash
/eventadmin setup wand
```
You will receive a Golden Axe named `§6UltraEvents Setup-Wand`.

#### 2. Select the Arena Bounds
* **Left-Click** a block to define **Position 1** (e.g., North-West lower corner of your play platform).
* **Right-Click** a block to define **Position 2** (e.g., South-East upper corner of your play platform).

*(Alternatively, stand at each position and use `/ea setup pos1` and `/ea setup pos2`.)*

#### 3. Set Spawns & Locations
Stand where you want players to be and execute:

* **Lobby Spawn** (where players wait before the event starts):
  ```bash
  /eventadmin setup lobby
  ```
* **Spectator Spawn** (where eliminated players watch the game):
  ```bash
  /eventadmin setup spectator
  ```
* **Exit Spawn** (where players are safely teleported back to your hub or spawn after the event finishes):
  ```bash
  /eventadmin setup exit
  ```

#### 4. Optional: Autodetect Heights
If your arena platform is built, run:
```bash
/eventadmin setup autodetect
```
This automatically calculates:
* `platform_y`: The playing surface level.
* `death_y`: 13 blocks below the platform (where players get eliminated).
* `lava_y`: 14 blocks below the platform.
* `ceiling_y`: 17 blocks above the platform.

#### 5. Verify & Save
Run:
```bash
/eventadmin setup check
```
If all checkmarks turn green (`✔`), finish by typing:
```bash
/eventadmin setup save
```
Your setup is permanently stored in `config.yml` and hot-reloaded immediately!

---

> [!IMPORTANT]
> ### 🛡️ Admin Pro-Tip: WorldGuard & Spawn Protection
> * **Vanilla Spawn Protection:** If your arena is near the world spawn point, ensure `spawn-protection=0` is set in your `server.properties`, otherwise non-OP players cannot interact with minigame blocks.
> * **WorldGuard Regions:** If you protect your arena with WorldGuard, ensure the region allows:
>   * `pvp: allow` (for combat modes like Sumo and One in the Chamber)
>   * `block-break: allow` (for Spleef)
>   * Alternatively, UltraEvents bypasses restrictions automatically for registered participants when using standard Bukkit events!
