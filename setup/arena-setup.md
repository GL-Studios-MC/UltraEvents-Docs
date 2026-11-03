# In-Game Setup Wizard & World Safety

With UltraEvents, you don't need to manually write coordinates into YAML files. The entire arena setup can be completed in-game in less than 60 seconds.

---

> [!CAUTION]
> ### ⚠️ Critical: How Arena Generation Works (Read Before Setup!)
> UltraEvents uses a **dynamic, automated block transformation and regeneration engine**.
> 
> * **Blocks are cleared and transformed:** The arena area between your **Position 1** and **Position 2** bounds will be continuously modified, replaced, and regenerated during matches (e.g., ColorFloor generates colored concrete patterns, TNT Run disintegrates floor blocks, and procedural modes generate new paths).
> * **DO NOT select your main server spawn or survival builds:** Setting `Pos1` and `Pos2` across player buildings, lobby structures, or survival towns will cause blocks in that region to be overridden by minigame mechanics!
> * **Best Practice Recommendation:** Always set up your event arena in a **dedicated world** (e.g., a void world named `Events` created via Multiverse) or at isolated coordinates (e.g., `X: 10000, Z: 10000`) safely separated from normal player structures.

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

### Generation Modes: Procedural vs. Snapshot

You can toggle between two arena generation types in `/eventadmin` or `config.yml`:

1. **`PROCEDURAL` (Default):**
   * The plugin automatically calculates and generates random obstacle courses, paths, and platform layouts every single round.
   * **Zero build maintenance:** You don't need to build arenas manually or paste schematics!

2. **`SNAPSHOT`:**
   * Takes a template snapshot of your hand-built custom arena structure and restores it cleanly between matches.

---

> [!IMPORTANT]
> ### 🛡️ WorldGuard & Spawn Protection
> * **Vanilla Spawn Protection:** If your arena is in the default world near coordinates `0, 0`, ensure `spawn-protection=0` is set in your `server.properties`, otherwise vanilla protection blocks non-OP players from minigame interactions.
> * **WorldGuard Regions:** If you protect your arena with WorldGuard, ensure the region allows `pvp: allow` and `block-break: allow` (for Spleef), or rely on UltraEvents' native bypass protection for registered event participants.
