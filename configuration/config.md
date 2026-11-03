# Main Configuration (config.yml)

The `config.yml` file allows you to customize the core behavior of UltraEvents.

---

### Key Configuration Sections

```yaml
# Plugin Language: 'en' (English - Default) or 'de' (German)
# Files located in plugins/UltraEvents/messages_xx.yml
language: "en"

# Maintenance Mode:
# When true, only staff members with 'ultraevents.team' (or OPs) can see and join events.
maintenance_mode:
  enabled: false
  permission: "ultraevents.team"

# Default Arena Settings
arena:
  world: "Events"
  platform_y: -42
  death_y: -55.0
  lava_y: -56
  ceiling_y: -25
  pos1:
    x: -390
    y: -42
    z: 4
  pos2:
    x: -295
    y: -42
    z: -77
  generation_type: "PROCEDURAL" # 'PROCEDURAL' or 'SNAPSHOT'
  difficulty: "NORMAL"          # 'LEICHT', 'NORMAL', 'SCHWER', 'HARDCORE'

# Event Defaults
event:
  mode: "COLOR_FLOOR"
  total_rounds: 3
  warmup_seconds: 7
```

---

### Voting System Settings

```yaml
voting:
  pause_rounds: 2 # How many rounds a mode rests after being played before it can be chosen again
  enabled_modes:
    COLOR_FLOOR: true
    TNT_RUN: true
    TNT_TAG: true
    RED_LIGHT_GREEN_LIGHT: true
    # (Additional PRO modes)
```

