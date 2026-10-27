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
