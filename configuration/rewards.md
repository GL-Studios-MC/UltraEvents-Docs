# Reward & Economy Engine

UltraEvents features a fully decoupled, universal reward distribution engine.

---

### Economy Integrations

1. **Vault Integration**:
   * Automatically deposits server currency for 1st, 2nd, and 3rd place finishers.
   * Also supports participation payout for everyone who stays until the end.

2. **PlayerPoints Integration**:
   * Soft-hook for servers using premium tokens or voting points.

3. **Custom Crate Keys**:
   * Define your server's crate keys in `config.yml`:
     ```yaml
     rewards:
       available_crates:
         - "Event"
         - "Legendary"
         - "Vote"
         - "Mythic"
     ```
   * Cycles automatically through your custom crate names in the in-game Admin GUI!

4. **Unlimited Console Commands**:
   * Execute custom commands on victory, supporting dynamic placeholders:
     * `%player%`: Winner's username
     * `%uuid%`: Winner's unique UUID
     * `%place%`: Placement rank (1, 2, or 3)
     * `%score%`: Total points scored

---

### Example Configuration

```yaml
rewards:
  min_players_for_top3: 4
  place_1:
    money: 2500.0
    crate_type: "Legendary"
    commands:
      - "lp user %player% permission settemp event.vip true 7d"
      - "broadcast &6%player% has won the event with %score% points!"
  place_2:
    money: 1000.0
    crate_type: "Event"
  place_3:
    money: 500.0
    crate_type: "Vote"
  participation:
    money: 100.0
```

