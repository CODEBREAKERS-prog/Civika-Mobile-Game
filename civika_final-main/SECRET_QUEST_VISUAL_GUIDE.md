# 🔐 SECRET QUEST SYSTEM - VISUAL GUIDE

## 🎯 Complete Feature Overview

```
┌─────────────────────────────────────────────────────────────┐
│                   SECRET QUEST SYSTEM                       │
│                                                             │
│  🔐 12 Secret Quests  |  👑 19 Unique Titles  |  🗺️ 5 Locations  │
└─────────────────────────────────────────────────────────────┘
```

---

## 📍 Map of Secret Locations (Barangay)

```
        BARANGAY MAP (Background-Relative Coordinates)
        
   0%                   50%                  100%
0% ┌─────────────────────────────────────────┐
   │ 🗺️ NW                        🗺️ NE     │  5%
   │ (5,5)                        (95,5)     │
   │                                          │
   │              The Wise Elder              │
   │                (12,88)                   │
50%│                   💎                     │
   │              Old Shrine                  │
   │                (50,85)                   │
   │      Scholar                Guardian     │
   │      (88,12)                (50,50)      │
   │                                          │
   │ 🗺️ SW                        🗺️ SE     │  95%
   │ (5,95)                       (95,95)    │
100%└─────────────────────────────────────────┘

Legend:
🗺️ = Secret Location (The Four Corners Quest)
💎 = Hidden Location (Hidden Paths Quest)
👤 = Hidden NPC (appears conditionally)
```

---

## 🎮 Player Journey Flow

```
START GAME
    │
    ▼
┌────────────────────────────────────┐
│   Explore the Barangay Map        │
│   Walk to Northwest Corner        │
└────────────────┬───────────────────┘
                 │
                 ▼
┌────────────────────────────────────┐
│  🔔 NOTIFICATION APPEARS           │
│  "🗺️ Secret Location Discovered!" │
│  "Northwest Sanctuary"             │
│  "A peaceful corner away from..."  │
└────────────────┬───────────────────┘
                 │
                 ▼
┌────────────────────────────────────┐
│  QUEST REVEALED IN SECRET MENU    │
│  🎯 "The Four Corners"             │
│  Progress: 1/4 (25%)               │
│  Hint: The edges of the map...    │
└────────────────┬───────────────────┘
                 │
                 ▼
┌────────────────────────────────────┐
│  Visit Other 3 Corners            │
│  NE → 2/4 (50%)                   │
│  SW → 3/4 (75%)                   │
│  SE → 4/4 (100%)                  │
└────────────────┬───────────────────┘
                 │
                 ▼
┌────────────────────────────────────┐
│  🏆 QUEST COMPLETED!               │
│  Title Unlocked: "Explorer"       │
│  +100 Coins, +200 Points          │
└────────────────┬───────────────────┘
                 │
                 ▼
┌────────────────────────────────────┐
│  TITLE EQUIPPED AUTOMATICALLY     │
│  HUD Now Shows: "👑 Explorer"      │
└────────────────────────────────────┘
```

---

## 🖥️ UI Layout with Secret Quests

### Full Screen Layout

```
┌─────────────────────────────────────────────────────────────┐
│ TOP-LEFT HUD:                    TOP-RIGHT HUD:            │
│ ┌──────────────┐                ┌──────────────────────┐  │
│ │ 👤 Alex      │                │ [📋] [🏪] [📅]       │  │
│ │ ⭐ L1        │                │ [🔐] [⏸️]  ← NEW!   │  │
│ ├──────────────┤                └──────────────────────┘  │
│ │ 👑 Explorer  │ ← NEW!                                   │
│ ├──────────────┤                                          │
│ │ 🏆 5/10      │                                          │
│ │ 💰 125       │                                          │
│ │ 📊 850       │                                          │
│ └──────────────┘                                          │
│                                                            │
│                    GAME WORLD                              │
│                  (Phaser Canvas)                           │
│                                                            │
│                                                            │
│ BOTTOM-LEFT:               BOTTOM-RIGHT:                  │
│ ┌──────────┐               ┌──────────┐                  │
│ │ 🕹️       │               │  [TAP]   │                  │
│ │ Joystick │               │ Interact │                  │
│ └──────────┘               └──────────┘                  │
│              (Mobile Only)                                 │
└─────────────────────────────────────────────────────────────┘
```

---

## 📋 Secret Quests Modal Layout

```
┌─────────────────────────────────────────────────────────┐
│  🔐 SECRET QUESTS                              [✕]      │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │         Current Title: Explorer                   │ │
│  │         "Discovered all corners of the map"       │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
│  ┌──────────────────┐  ┌──────────────────┐           │
│  │ 🎯 Secret Quests │  │   👑 Titles      │           │
│  │   (ACTIVE)       │  │                  │           │
│  └──────────────────┘  └──────────────────┘           │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ ✅ The Four Corners                               │ │
│  │ Visit all 4 corners of the map                    │ │
│  │ ████████████████████ 100%                         │ │
│  │ 💰 +100  ⭐ +200    👑 Explorer                    │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ 🎯 Master Collector                               │ │
│  │ Collect ALL items in both maps                    │ │
│  │ ██████░░░░░░░░░░░░░ 28% (5/18)                    │ │
│  │ Hint: 💎 Every treasure tells a story...          │ │
│  │ 💰 +300  ⭐ +500    👑 Treasure Hunter             │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ 🔐 Discover secrets to unlock unique titles!      │ │
│  │ 2 / 12 secrets discovered                         │ │
│  └───────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────┘
```

---

## 👑 Titles Tab Layout

```
┌─────────────────────────────────────────────────────────┐
│  🔐 SECRET QUESTS                              [✕]      │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │         Current Title: Explorer                   │ │
│  │         "Discovered all corners of the map"       │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
│  ┌──────────────────┐  ┌──────────────────┐           │
│  │ 🎯 Secret Quests │  │   👑 Titles      │           │
│  │                  │  │   (ACTIVE)       │           │
│  └──────────────────┘  └──────────────────┘           │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ 👑 Citizen                              ✅        │ │
│  │ A member of the community                         │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ 👑 Explorer                                       │ │
│  │ Discovered all corners of the map                 │ │
│  │                    💙 UNCOMMON                     │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ 👑 Treasure Hunter        🔒 LOCKED               │ │
│  │ Collected all treasures                           │ │
│  │                    💜 RARE                         │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ 🔐 Unlock titles by completing secret quests!     │ │
│  │ 2 / 19 titles unlocked                            │ │
│  └───────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────┘
```

---

## 🗺️ Discovery Notification

```
┌──────────────────────────────────────┐
│  🗺️ Secret Location Discovered!     │
├──────────────────────────────────────┤
│                                      │
│  You found: Northwest Sanctuary      │
│                                      │
│  "A peaceful corner away from        │
│   the bustle"                        │
│                                      │
│  Quest Progress Updated!             │
│  The Four Corners: 1/4               │
│                                      │
│         [Amazing!]                   │
└──────────────────────────────────────┘
```

---

## 🏆 Quest Completion Notification

```
┌──────────────────────────────────────┐
│  🏆 Secret Quest Completed!          │
├──────────────────────────────────────┤
│                                      │
│  Quest: The Four Corners             │
│                                      │
│  ✨ Title Unlocked: Explorer         │
│                                      │
│  Rewards:                            │
│  💰 +100 Coins                       │
│  ⭐ +200 Points                      │
│                                      │
│  Your title is now equipped!         │
│                                      │
│         [Continue Exploring]         │
└──────────────────────────────────────┘
```

---

## 🎮 Complete Navigation (Updated)

```
                    MAIN MENU
                        │
        ┌───────────────┼───────────────┐
        │               │               │
   New Game      Leaderboard       Settings
        │                              Extras
        ▼                            Credits
  Character Creation
        │
        ▼
   GAME WORLD (BarangayMap/CityMap)
        │
  ┌─────┴─────┬─────────┬──────────┬──────────┬─────────┐
  │           │         │          │          │         │
SPACE      📋 Quest  🏪 Shop   📅 Daily  🔐 Secrets  ⏸️ Menu
  │           │         │          │          │         │
  ▼           ▼         ▼          ▼          ▼         ▼
Mission   Quest Log  Shop   Daily     SECRET    Pause Menu
System               Modal  Challenges QUESTS      │
  │                                   MODAL        │
  ▼                                                ├─> Quest Log
Quiz System                                        ├─> Inventory
  │                                                ├─> Shop
  ▼                                                ├─> Daily
Complete                                           ├─> SECRET QUESTS
  │                                                ├─> Leaderboard
  └─> Check Secret Quest Conditions                └─> Restart
```

---

## 📊 Title Rarity Progression

```
🤍 COMMON
┌──────────────┐
│   Citizen    │  ← Default starting title
└──────────────┘

        ↓ Complete easy secrets

💙 UNCOMMON
┌──────────────┬──────────────┬──────────────┐
│   Explorer   │Coin Collector│Lightning Mind│
└──────────────┴──────────────┴──────────────┘
        ↓ Complete challenging secrets

💜 RARE
┌──────────────┬──────────────┬──────────────┐
│ Pathfinder   │Treasure Hunter│ Speedrunner │
│  Civic Sage  │  Hidden Hero  │             │
└──────────────┴──────────────┴──────────────┘
        ↓ Complete ultimate challenges

🟡 LEGENDARY
┌──────────────┬──────────────┬──────────────┐
│   Legend     │Perfect Citizen│Master Civics│
│Mysterious One│               │             │
└──────────────┴──────────────┴──────────────┘
```

---

## 🎯 Quest Type Breakdown

```
SECRET QUESTS (12 Total)
│
├─ 🗺️ EXPLORATION (2)
│  ├─ The Four Corners
│  └─ Hidden Paths
│
├─ 💎 COLLECTION (2)
│  ├─ Master Collector
│  └─ Golden Hoarder
│
├─ ⚡ SPEED (2)
│  ├─ Lightning Campaign
│  └─ Thunder Mind
│
├─ 💬 INTERACTION (2)
│  ├─ Community Connector
│  └─ The Wise One
│
├─ 🏆 ACHIEVEMENT (2)
│  ├─ Perfect Civic Leader
│  └─ The Legend
│
└─ 🎮 EASTER EGG (2)
   ├─ The Hidden Message
   └─ The Konami Code
```

---

## 🎨 Title Display Variations

### In HUD (Top-Left)

**Common Title:**
```
┌─────────────┐
│ 👤 Alex     │
│ ⭐ L1       │
│ 👑 Citizen  │  ← Gray gradient
│ 🏆 5/10     │
└─────────────┘
```

**Uncommon Title:**
```
┌─────────────┐
│ 👤 Maria    │
│ ⭐ L2       │
│ 👑 Explorer │  ← Blue gradient
│ 🏆 15/20    │
└─────────────┘
```

**Rare Title:**
```
┌────────────────────┐
│ 👤 Juan            │
│ ⭐ L2              │
│ 👑 Treasure Hunter │  ← Purple gradient
│ 🏆 18/20           │
└────────────────────┘
```

**Legendary Title:**
```
┌─────────────┐
│ 👤 Ana      │
│ ⭐ L2       │
│ 👑 Legend   │  ← Gold gradient, animated!
│ 🏆 20/20    │
└─────────────┘
```

---

## 🔄 Secret Quest State Flow

```
┌─────────────┐
│   HIDDEN    │  ← Quest exists but player hasn't discovered
│   ❓ ???    │     Shows as "???" in list (if visible at all)
└──────┬──────┘
       │
       │ Player meets discovery condition
       ▼
┌─────────────┐
│ DISCOVERED  │  ← Quest revealed but not completed
│  🎯 Active  │     Shows name, description, hints
└──────┬──────┘     Progress bar appears
       │
       │ Player completes all conditions
       ▼
┌─────────────┐
│ COMPLETED   │  ← Quest finished
│ ✅ Done     │     Title awarded
└──────┬──────┘     Rewards given
       │
       │ Quest completion triggers
       ▼
┌─────────────┐
│TITLE AWARDED│  ← Title added to collection
│  👑 New!    │     Can be equipped
└──────┬──────┘     Shows in HUD when active
       │
       │ Player equips title
       ▼
┌─────────────┐
│   ACTIVE    │  ← Title displayed in HUD
│  ✨ Shown   │     Visible to player
└─────────────┘
```

---

## 🎯 Example: "The Four Corners" Quest

### Step-by-Step Visual

**Step 1: Discover Location**
```
Player at: (5%, 5%)
         ↓
   🚶 → 🗺️ (Northwest Sanctuary)
         ↓
   Notification: "Secret Location Discovered!"
         ↓
   Quest "The Four Corners" revealed
```

**Step 2: Track Progress**
```
Visit NW (5,5):   ████░░░░░░░░░░░░ 25%
Visit NE (95,5):  ████████░░░░░░░░ 50%
Visit SW (5,95):  ████████████░░░░ 75%
Visit SE (95,95): ████████████████ 100% ✅
```

**Step 3: Receive Reward**
```
🏆 Quest Complete!
   ↓
👑 Title: "Explorer" unlocked
   ↓
💰 +100 coins
⭐ +200 points
   ↓
Title auto-equipped
   ↓
HUD now shows: "👑 Explorer"
```

---

## 🎮 Button Locations Reference (Updated)

### HUD Buttons (Top-Right) - NOW 5 BUTTONS!

```
BEFORE:                    AFTER (NEW):
┌────────────────┐        ┌────────────────────────┐
│ [📋] [🏪]      │        │ [📋] [🏪] [📅]        │
│ [📅] [⏸️]      │   →    │ [🔐] [⏸️]  ← NEW!    │
└────────────────┘        └────────────────────────┘
```

### Pause Menu Options - NOW 8 OPTIONS!

```
BEFORE:                    AFTER (NEW):
1. ▶️ Resume               1. ▶️ Resume
2. 📋 Quest Log            2. 📋 Quest Log
3. 🎒 Inventory            3. 🎒 Inventory
4. 🏪 Shop                 4. 🏪 Shop
5. 📅 Daily Challenges     5. 📅 Daily Challenges
6. 🏆 Leaderboard          6. 🔐 Secret Quests  ← NEW!
7. 🔄 Restart              7. 🏆 Leaderboard
                           8. 🔄 Restart
```

---

## 🔍 Quest Discovery Triggers

```
EXPLORATION QUESTS:
┌────────────────────────────────────┐
│ Walk to location → Auto-discover   │
│ Proximity: 5% radius               │
│ Example: Visit (5,5) for NW corner │
└────────────────────────────────────┘

COLLECTION QUESTS:
┌────────────────────────────────────┐
│ Collect items → Progress updates   │
│ Checked automatically              │
│ Example: 18/18 items → Complete    │
└────────────────────────────────────┘

SPEED QUESTS:
┌────────────────────────────────────┐
│ Complete in time → Quest unlocks   │
│ Checked on mission complete        │
│ Example: All missions <2hr → Done  │
└────────────────────────────────────┘

INTERACTION QUESTS:
┌────────────────────────────────────┐
│ Talk to NPCs → Progress tracks     │
│ Hidden NPCs appear conditionally   │
│ Example: 3 hidden NPCs → Complete  │
└────────────────────────────────────┘

ACHIEVEMENT QUESTS:
┌────────────────────────────────────┐
│ Meet conditions → Auto-check       │
│ Multiple requirements              │
│ Example: 100% + perfect → Complete │
└────────────────────────────────────┘

EASTER EGG QUESTS:
┌────────────────────────────────────┐
│ Discover secret → Quest reveals    │
│ Special sequences/locations        │
│ Example: Visit NPCs in order       │
└────────────────────────────────────┘
```

---

## 💡 Player Progression Path

```
NEW PLAYER
    │
    ▼
┌─────────────────────────────────────┐
│ 👑 Citizen (Default)                │
│ "Just started the journey"          │
└───────────┬─────────────────────────┘
            │
            │ Explore corners
            ▼
┌─────────────────────────────────────┐
│ 👑 Explorer (Uncommon)              │
│ "Found all map corners"             │
└───────────┬─────────────────────────┘
            │
            │ Collect all items
            ▼
┌─────────────────────────────────────┐
│ 👑 Treasure Hunter (Rare)           │
│ "Collected all treasures"           │
└───────────┬─────────────────────────┘
            │
            │ Complete all quests fast
            ▼
┌─────────────────────────────────────┐
│ 👑 Speedrunner (Rare)               │
│ "Finished in record time"           │
└───────────┬─────────────────────────┘
            │
            │ Complete ALL secret quests
            ▼
┌─────────────────────────────────────┐
│ 👑 Legend (Legendary)               │
│ "THE ULTIMATE ACHIEVEMENT"          │
└─────────────────────────────────────┘
```

---

## 📱 Mobile vs Desktop View

### Mobile (Compact)

```
┌───────────────────────────┐
│ TOP-LEFT (Vertical Stack):│
│ ┌───────────┐             │
│ │👤 Alex ⭐L1│            │
│ ├───────────┤             │
│ │👑 Explorer│             │
│ ├───────────┤             │
│ │🏆5 💰125  │             │
│ └───────────┘             │
│                           │
│ TOP-RIGHT (Compact):      │
│ [📋][🏪][📅]             │
│ [🔐][⏸️]  ← Icons only   │
│                           │
│   GAME WORLD              │
│                           │
│ [🕹️]          [TAP]      │
└───────────────────────────┘
```

### Desktop (Full)

```
┌────────────────────────────────────────┐
│ TOP-LEFT:           TOP-RIGHT:         │
│ 👤 Alex            [📋 Quest]          │
│ ⭐ L1              [🏪 Shop]            │
│ 👑 Explorer        [📅 Daily]          │
│ 🏆 5/10            [🔐 Secrets] ← NEW! │
│ 💰 125             [⏸️ Menu]           │
│ 📊 850                                 │
│                                        │
│          GAME WORLD (Larger)           │
│                                        │
└────────────────────────────────────────┘
```

---

## 🎯 Quick Reference Card

### Access Secret Quests:
```
HUD: Click [🔐]
ESC Menu: Click [🔐 Secret Quests]
```

### First Secret (Easy):
```
1. Walk to (5%, 5%) - Northwest corner
2. See discovery notification
3. Visit 3 more corners
4. Unlock "Explorer" title
```

### Change Title:
```
1. Open [🔐 Secrets]
2. Click "Titles" tab
3. Click any unlocked title
4. See it in HUD!
```

---

## 🏆 Achievement Checklist

```
□ Visit all 4 corners          → 👑 Explorer
□ Collect all 18 items         → 👑 Treasure Hunter
□ Earn 1,000 total coins       → 👑 Coin Collector
□ Complete in <2 hours         → 👑 Speedrunner
□ Talk to all NPCs 3x          → 👑 Social Butterfly
□ Find 3 hidden NPCs           → 👑 Civic Sage
□ Get 100% completion          → 👑 Perfect Citizen
□ Complete ALL secret quests   → 👑 Legend
```

---

## 🎉 Summary Diagram

```
┌─────────────────────────────────────────────────────┐
│        SECRET QUEST SYSTEM COMPLETE                 │
├─────────────────────────────────────────────────────┤
│                                                     │
│  ✅ 12 Secret Quests    ✅ 19 Player Titles        │
│  ✅ 5 Hidden Locations  ✅ 3 Hidden NPCs           │
│  ✅ Full UI Integration ✅ Progress Tracking       │
│  ✅ HUD Title Display   ✅ Quest Hints             │
│  ✅ Auto-Discovery      ✅ Rarity System           │
│  ✅ Persistent Storage  ✅ Complete Docs           │
│                                                     │
│  🎮 READY TO PLAY! 🎮                              │
└─────────────────────────────────────────────────────┘
```

---

**Last Updated**: October 10, 2025  
**Version**: 1.0.0  
**Status**: ✅ Complete

**🔐 The mysteries await, brave citizen! ✨**

