# Commands & Permissions

UltraEvents provides a streamlined set of player and administrator commands.

---

### Player Commands

| Command | Aliases | Permission | Description |
| :--- | :--- | :--- | :--- |
| `/ultraevents` | `/ue`, `/events`, `/event` | `ultraevents.use` | Opens the main Player Event Hub GUI. |
| `/beitreten` | `/eventjoin`, `/join` | `ultraevents.use` | Instantly joins the currently active or waiting event. |

---

### Admin Commands

All administrator features require the `ultraevents.admin` permission (given to OPs by default).

| Command | Aliases | Description |
| :--- | :--- | :--- |
| `/eventadmin` | `/ea`, `/ueadmin` | Opens the main Admin Control Center GUI. |
| `/eventadmin start` | `/ea start` | Forces the start of the event countdown. |
| `/eventadmin stop` | `/ea stop` | Immediately aborts the current match and resets the arena. |
| `/eventadmin setup` | `/ea setup` | Shows setup instructions and check status. |
| `/eventadmin setup wand` | `/ea setup wand` | Gives the visual wand tool for corner selection. |
| `/eventadmin setup pos1` | `/ea setup pos1` | Sets arena corner 1 at your feet. |
| `/eventadmin setup pos2` | `/ea setup pos2` | Sets arena corner 2 at your feet. |
| `/eventadmin setup lobby` | `/ea setup lobby` | Sets the lobby spawnpoint at your feet & eye direction. |
| `/eventadmin setup spectator` | `/ea setup spectator` | Sets the spectator spawnpoint. |
| `/eventadmin setup exit` | `/ea setup exit` | Sets the exit return location when an event ends. |
| `/eventadmin setup check` | `/ea setup check` | Tests your configuration for missing values. |
| `/eventadmin setup save` | `/ea setup save` | Saves arena bounds to `config.yml`. |

---

### Permissions Hierarchy

* `ultraevents.use` (Default: `true` for all players): Allows opening the player GUI and participating in events.
* `ultraevents.team` (Default: `op`): Allows staff members to join during **Maintenance Mode** (`maintenance_mode: true`).
* `ultraevents.admin` (Default: `op`): Full access to the setup system, game control, and reward management.

