# Blockfront Arena

A browser-based voxel arena game with wave combat, bosses, upgrades, unlockable skins, save/resume, and local two-player co-op.

## Play

Open the GitHub Pages link in a modern desktop browser.

## Controls

- Solo: WASD or arrow keys to move
- Aim: mouse
- Fire: mouse button or R
- Dash: Space
- Pause: P
- Local co-op: Player 1 uses WASD + R; Player 2 uses arrow keys + Enter

LAN mode requires the separate local server and is not available through GitHub Pages.

## Combat supplies upgrade

Open `index.html` in a desktop browser to play offline. No installation required.

Buy Combat Supplies in the lobby or between waves. Purchases use earned game coins. Unused stock persists across runs and reloads.

| Supply | Price | Control | Effect |
| --- | --- | --- | --- |
| Aegis Shield | 40 coins | 1 or Q | 8 seconds of protection, shared in local co-op |
| Prism Laser | 60 coins | 2 or E | Mouse-aimed piercing beam, 12× weapon damage, bypasses armor |
| Mega Bomb | 100 coins | 3 or B | Arena-wide 25× weapon damage; clears hostile shots and enemy armor |

Supplies also have clickable buttons during combat. Repeat shield activations extend its duration.

Skins multiply end-of-run coin rewards from 1× for Neon Scout to 100× for Omega Sovereign. Each skin shows its multiplier in the shop. The run retains its starting multiplier when saved and resumed. Existing saves and purchases remain compatible. LAN supplies are disabled; local co-op is supported.

Run logic checks with `node tests/game.cjs`.

Premium skins: Inferno Overlord (25,000 coins, 15×), Storm Titan (50,000, 20×), Nebula Monarch (100,000, 30×), Singularity Phantom (250,000, 45×), Eternal Seraph (500,000, 65×), Omega Sovereign (1,000,000, 100×). Each has a unique projectile color.

## World progression

Use Worlds in the lobby to select a destination for your next solo or local co-op run.

| World | Lifetime coins required | Enemy health | Enemy movement speed |
| --- | ---: | ---: | ---: |
| Neon Foundry | 0 | Normal | Normal |
| Glacier Station | 100,000 | +8% | Normal |
| Ember Forge | 250,000 | +16% | +3% |
| Overgrown Reactor | 500,000 | +24% | +5% |
| Astral Vault | 1,000,000 | +32% | +8% |

Coins earned at the end of runs count toward permanent world unlocks. Unlocks are free; purchases do not reduce progress. Existing saves begin lifetime tracking from the current coin balance because older earnings were not recorded. New worlds change the default scenery and boss theme; visual settings can still override the scenery. Player stats, weapon power, enemy damage, and coin rates receive no world bonuses. Saved runs keep their original world, including old saves which default to Neon Foundry. Each world tracks its best cleared wave. Bosses show a visual warning before special attacks.
