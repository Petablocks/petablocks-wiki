# 🛡️ Staff Handbook & Moderation SOP

This confidential guide outlines Standard Operating Procedures (SOP), communication protocols, and moderation standards for the PETABLOCKS Staff Team.

---

## 1. Core Principles
1. **Remain Impartial**: Treat every player with professional respect, regardless of personal opinions or past incidents.
2. **Collect Evidence First**: Always take screenshots or record video evidence before issuing bans or long mutes. Log evidence in the `#staff-logs` Discord channel.
3. **De-escalate**: Defuse arguments calmly. Avoid engaging in public arguments in global chat.
4. **Never Abuse Powers**: Staff permissions (spectator, creative mode, item spawning, teleports) are strictly for moderation tasks. Any unauthorized use will lead to immediate demotion.

---

## 2. Moderation Workflow

```
[Player Report / Violation Observed]
               │
               ▼
   [Gather Evidence (Screenshots/Logs)]
               │
               ▼
   [Consult Punishment Escalation Matrix]
               │
               ▼
   [Execute Moderation Command + Provide Reason]
               │
               ▼
   [Post Log & Evidence in #staff-logs Discord]
```

---

## 3. Standard Moderation Commands

| Action | Syntax | Example |
|---|---|---|
| **Kick** | `/kick <player> <reason>` | `/kick Player123 Inappropriate skin (Please change)` |
| **Mute** | `/mute <player> <duration> <reason>` | `/mute Player123 1h Excessive toxicity in main chat` |
| **Temp Ban** | `/tempban <player> <duration> <reason>` | `/tempban Player123 3d Griefing player base (Ticket #42)` |
| **Permanent Ban** | `/ban <player> <reason>` | `/ban Player123 X-Ray / Unapproved Hacked Client` |
| **Inventory Inspect** | `/invsee <player>` | `/invsee Player123` |
| **Vanish** | `/v` or `/vanish` | Enables invisible moderation mode |

---

## 4. Rollback & Grief Investigation
- Inspect container transactions and block placements using CoreProtect/Log tools (`/co i` or inspection tool).
- To rollback griefing within a specific claim:
  ```
  /co rollback u:<griefer_name> t:24h r:30
  ```
- Always verify affected boundaries before running a global rollback.

---

## 5. Escalation & Incident Response
- **Server Lag / TPS Drops**: Use `/tps` and `/spark` to profile memory or tick loops. Notify senior admins if lag exceeds 5 minutes.
- **Critical Exploit / Duping**: Immediately freeze the player (`/freeze <player>`) and ping `@Owner` in staff Discord.
