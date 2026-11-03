# Troubleshooting & FAQ

Common questions, tips, and resolutions for UltraEvents.

---

### FAQ

#### 1. Does UltraEvents work on Folia?
**Yes.** UltraEvents does not rely on outdated global scheduler calls. It includes a native abstraction layer that automatically uses Folia's `GlobalRegionScheduler` and `AsyncScheduler` when running on a Folia server.

#### 2. What happens if a player leaves during an event?
UltraEvents tracks disconnected players. If a player disconnects mid-round, they are safely eliminated without breaking game state or causing null pointers. When they reconnect, they will not be stuck inside arena hazards.

#### 3. How do I switch languages?
Open `config.yml` and change:
```yaml
language: "de" # For German
# or
language: "en" # For English
```
Then run `/eventadmin reload` or restart your server.

#### 4. Can I use custom items as rewards?
**Yes!** Hold any item in your main hand and type `/eventadmin` -> Click **Belohnungs-Status**. Click **Item in Hand als Siegerpreis setzen**. The exact item with all enchantments, custom lore, and NBT tags will be awarded to 1st place!

---

### Need further help?

* Join our official Discord community: **GL Studios Community Discord**
* Report bugs or request new mini-games via support tickets.

