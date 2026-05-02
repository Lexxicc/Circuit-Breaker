# Circuit Breaker: Defusal Unit — Ruleset

> Keep this file in sync with the How to Play page in `Circuit Breaker.html` whenever rules or mechanics change.

---

## Goal

Enclose all **25 cells** on a 5×5 grid by placing wires before the **3-minute** countdown expires.

---

## Controls

- **Click / tap a line** between two dots to place a wire
- **ABORT** — return to main menu

---

## The Wire Cycle

Every three moves follow a fixed cycle — you cannot deviate:

| Move | Wire type |
|---|---|
| 1 | Override Wire (teal) |
| 2 | Override Wire (teal) |
| 3 | Red Surge Wire (red) |

The status panel always shows which wire comes next. The cycle repeats until all lines are placed.

---

## The Grid

- 6×6 dots — 5×5 cells (25 total)
- 60 lines total (30 horizontal, 30 vertical)
- Perimeter border lines are blocked — you cannot place wires there
- Some interior lines are pre-blocked as obstacles (~22% chance per line; min 10 playable lines guaranteed)

---

## Cell Scoring

A cell is **closed** when all 4 of its sides have a wire.

| Cell state | Condition | Points |
|---|---|---|
| SAFE | Closed with no red surge wires on any side | +1 |
| DETECTED | Closed but at least one side is a red surge wire | 0 |

Red surge wires poison any cell they border — even if the other 3 sides are override wires.

---

## Win / Loss

| Condition | Result |
|---|---|
| All 25 cells enclosed before time runs out | **Defused** — score saved |
| Timer reaches 0:00 | **Detonated** — score saved as a loss |

---

## Scoring

| Component | Value |
|---|---|
| Safe cells | 1 pt each (max 25) |
| Speed bonus | `floor(Seconds Remaining / 10) × 0.5` — win only |

---

## Score Tiers

| Tier | Score |
|---|---|
| Gold | 20+ |
| Silver | 12–19 |
| Bronze | 5–11 |

---

## Challenge Mode

- After winning, copy a challenge link — your opponent plays the identical seeded board
- Both scores are compared; result shows **WIN / LOSE / DRAW**
- Challenge links expire after **72 hours**

---

## Named Missions

20 fixed seeded boards: ALPHA-1, BETA-4, GAMMA-9, SIGMA-X, OMEGA-0, NEON-2, CYBER-5, VOID-8, PRIME-1, TITAN-K, GHOST-V, HYPER-6, SOLO-Q, NEXUS-M, ZERO-G, STORM-Z, QUARTZ, PULSE-W, ZENITH, BLADE-9.

Random games use a fresh seed each time.

---

Last updated: 2026-05-02 — v0.0.9
