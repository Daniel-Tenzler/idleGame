IDLE GAME DESIGN DOCUMENT
TABLE OF CONTENTS

1. EXECUTIVE SUMMARY
2. GAME OVERVIEW
3. TARGET AUDIENCE
4. CORE LOOP
5. SKILL SYSTEM
6. COMBAT SYSTEM
7. EQUIPMENT SYSTEM
8. ECONOMY & RESOURCES
9. PROGRESSION SYSTEM
10. MONSTER DESIGN
11. USER INTERFACE
12. TECHNICAL REQUIREMENTS
13. MVP SCOPE
14. DEVELOPMENT PHASING

---

1. EXECUTIVE SUMMARY
A hardcore idle game focused on long-term progression through skill specialization and resource management. Players engage in time-based actions across 9 interconnected skills to build character power, craft equipment, and defeat increasingly difficult monsters. The game emphasizes deliberate decision-making, strategic resource allocation, and satisfying power fantasy progression over short sessions.
Key Features:

- 9 interconnected skills with resource dependencies
- Progressive monster combat system
- Deep equipment crafting and upgrade paths
- Long-term progression with exponential scaling
- Resource economy with multiple interlocking systems

---

1. GAME OVERVIEW
Game Vision
Create a deep, complex idle game for hardcore players who enjoy methodical progression and strategic resource management. The game rewards long-term planning and deliberate skill investment rather than rapid advancement.
Core Fantasy
Players become masters of multiple disciplines, gradually building from raw resource gathering to powerful combat capability and advanced equipment crafting.
Platform & Technology

- Platform: Web-based
- Frontend: React with Vite and Tailwind CSS
- Monetization: None (MVP)
- Session Length: 15-30 minutes active playtime

---

1. TARGET AUDIENCE
Primary Audience: Hardcore idle gamers

- Appreciates complexity and depth
- Enjoys long-term progression systems
- Values strategic decision-making
- Familiar with games like NGU Idle and Idle Cultivation
- Prefers meaningful progression over rapid advancement
Player Expectations:
- Time-intensive progression (10-30 second actions, hours to level)
- Complex resource dependencies
- Multiple progression paths
- Satisfying endgame content

---

1. CORE LOOP
Primary Loop
1. Gather Resources (Mining, Herbalism, Forestry, Hunting)
1. Process Resources (Smithing, Alchemy, Woodworking, Tailoring)  
1. Craft/Upgrade Equipment
1. Fight Monsters
1. Unlock New Content
1. Repeat with Enhanced Capabilities
Secondary Loop

- Skill Specialization: Focus XP into specific skills for faster advancement
- Resource Allocation: Choose between immediate benefits vs long-term investment
- Equipment Optimization: Balance offense, defense, and utility

---

1. SKILL SYSTEM
Skill Overview
9 interconnected skills with resource dependencies and level-based unlocks.
Skill Actions & Progression
Attack Skill

- Core Action: Train Combat (20s, 5 Attack XP, 1 Weapon durability)
- Level 5 Unlock: Focused Training (45s, 25 Attack XP, 2 Weapon durability, 10 Gold)
- Combat Impact: Auto-attack every 2 seconds, +10% damage per level
Magic Skill
- Core Action: Practice Magic (25s, 6 Magic XP, 10 Mana)
- Spell Progression:
  - Level 3: Firebolt (8s cooldown, 12 Magic XP)
  - Level 7: Frost Shield (15s cooldown, 18 Magic XP)
  - Level 12: Lightning Strike (25s cooldown, 30 Magic XP)
  - Level 18: Arcane Intellect (30s cooldown, 40 Magic XP)
- Combat Impact: Special attacks with cooldowns, +15% magic damage per level
Mining (No Cost Actions)
- Level 1: Mine Copper (15s, 3 Mining XP, 1-3 Copper Ore)
- Level 6: Mine Iron (20s, 5 Mining XP, 1-2 Iron Ore)
- Level 11: Mine Steel (25s, 8 Mining XP, 1 Steel Ore)
- Level 16: Mine Mithril (35s, 15 Mining XP, 1 Mithril Ore)
Smithing
- Level 1: Forge Bronze Sword (30s, 8 XP, 5 Copper Ore + 2 Tin Ore + 10 Gold)
- Level 6: Forge Iron Armor (45s, 15 XP, 8 Iron Ore + 2 Silver Ore + 25 Gold)
- Level 11: Forge Steel Weapon (60s, 25 XP, 5 Steel Ore + 1 Gold Ore + 50 Gold)
- Level 16: Forge Mithril Gear (90s, 50 XP, 3 Mithril Ore + 1 Adamantite Ore + 100 Gold)
Herbalism (No Cost Actions)
- Level 1: Gather Common Herbs (12s, 2 XP, 2-4 Common Herb)
- Level 6: Gather Forest Herbs (18s, 4 XP, 1-3 Rare Herb)
- Level 11: Gather Mystic Herbs (25s, 7 XP, 1-2 Epic Herb)
- Level 16: Gather Enchanted Herbs (35s, 12 XP, 1 Legendary Herb)
Alchemy
- Level 1: Brew Strength Potion (25s, 10 XP, 3 Common Herb + 1 Glass Bottle)
- Level 5: Brew Mana Potion (30s, 15 XP, 2 Common Herb + 1 Rare Herb + 1 Glass Bottle)
- Level 11: Brew Permanent Elixir (60s, 40 XP, 5 Rare Herb + 2 Epic Herb + 1 Glass Bottle)
- Level 15: Brew Skill Boost (45s, 35 XP, 3 Epic Herb + 1 Gold Dust)
Forestry (No Cost Actions)
- Level 1: Chop Oak Trees (18s, 3 XP, 2-4 Oak Wood, +1 HP per level)
- Level 6: Chop Pine Trees (24s, 5 XP, 1-3 Pine Wood, +2 HP per level)
- Level 11: Chop Ebony Trees (32s, 9 XP, 1-2 Ebony Wood, +4 HP per level)
- Level 16: Chop Yggdrasil Saplings (45s, 18 XP, 1 Yggdrasil Wood, +8 HP per level)
Woodworking
- Level 1: Craft Spear (35s, 10 XP, 5 Oak Wood + 10 Gold)
- Level 6: Craft Longbow (50s, 20 XP, 5 Pine Wood + 25 Gold)
- Level 11: Craft Ebony Staff (70s, 35 XP, 3 Ebony Wood + 50 Gold)
- Level 16: Craft Yggdrasil Wand (100s, 60 XP, 2 Yggdrasil Wood + 100 Gold)
Hunting (No Cost Actions)
- Level 1: Hunt Rabbits (20s, 4 XP, 1-2 Basic Hide + 1 Rabbit Meat)
- idle Game
- Level 6: Hunt Deer (28s, 7 XP, 1 Quality Hide + 2 Deer Meat)
- Level 11: Hunt Bears (40s, 12 XP, 1 Superior Hide + 3 Bear Meat, 10% Bear Claw)
- Level 16: Hunt Magical Beasts (55s, 25 XP, 1 Enchanted Hide + 5 Mythic Meat, 25% Magical Essence)
Tailoring
- Level 1: Sew Apprentice Robes (40s, 12 XP, 3 Basic Hide + 1 Common Thread + 15 Gold)
- Level 6: Sew Mage Robes (60s, 25 XP, 2 Quality Hide + 1 Rare Thread + 30 Gold)
- Level 11: Sew Wizard Robes (90s, 45 XP, 1 Superior Hide + 1 Epic Thread + 1 Magical Essence + 50 Gold)
- Level 16: Sew V7 Craft Archmage Robes (120s, 80 XP, 1 Enchanted Hide + 1 Mythic Thread + 2 Magical Essence + 100 Gold)
Level Requirements
- Level 1: 0 XP (starting point)
- Level 2: 20 XP
- Level 3: 50 XP
- Level 4: 90 XP
- Level 5: 140 XP
- Level 6: 200 XP
- Level audience:
  - Level 7: 280 XP
  - Level 8: 380 XP
  - Layout: 500 XP
  - Level 10: 640 XP
  - Level 11: 800 XP
  - Level 12: 1000 XP
  - Level 13: 1240 XP
  - Level 14: 1520 XP
  - Level 15: 1840 XP
  - Level 16: 2200 XP
  - Level 17: 2640 XP
  - Level 18: 3140 XP
  - Level 19: 3700 XP
  - Level 20: 4400 XP
Duration Scaling
- Gathering Skills: No costs, level-based unlocks
- Craft Skills: Resource consumption, produce value
- Combat Skills: Equipment consumption, direct combat benefits

---

1. COMBAT SYSTEM
Auto-Attack Mechanics

- Frequency: Every 2 seconds
- Damage Calculation: Base damage × (1 + Attack level × 0.1)
- Level Bonus: +10% damage per level
Magic System
- Spell Cooldowns: 5-25 seconds based on spell type
- Damage Calculation: Base magic damage × (1 + Magic level × 0.15)
- Level Bonus: +15% magic damage, -0.5s cooldown per level
Combat Flow

1. Select unlocked monster
2. Auto-attacks engage continuously
3. Player activates magic abilities on cooldown
4. Combat continues until monster dies or player switches targets
5. No penalty for losing (time investment only)

---

1. EQUIPMENT SYSTEM
Quality Tiers

- Common (White): +10% stats
- Uncommon (Green): +25% stats
- Rare (Blue): +50% stats
- Epic (Purple): +100% stats
- Legendary (Gold): +200% stats
Equipment Slots
- Weapon: Attack/Magic damage
- Armor: Defense/HP
- Accessory: Various bonuses
- Magic Item: Spell power/Cooldown reduction
Equipment Sources
- Crafting: Smithing, Woodworking, Tailoring
- Monster Drops: Random loot tables per monster
- Shop: Gold purchases for convenience

---

1. ECONOMY & RESOURCES
Resource Flow
Mining → Ore → Smithing → Equipment
Herbalism → Herbs → Alchemy → Buffs
Forestry → Wood → Woodworking → Items → Gold
Hunting → Hides → Tailoring → Magic Equipment
Gold → Shop → Various Purchases
Resource Types

- Ore: Copper, Tin, Iron, Silver, Steel, Gold, Mithril, Adamantite
- Herbs: Common, Rare, Epic, Legendary, Mythic
- Wood: Oak, Pine, Ebony, Yggdrasil
- Hides: Basic, Quality, Superior, Enchanted
- Crafting Components: Glass Bottles, Thread, Magical Essence
- Currency: Gold
Gold Sinks
- Instant skill level-ups (expensive, scaling cost)
- Pre-crafted equipment
- Resource bundles
- Tool repairs

---

1. PROGRESSION SYSTEM
Character Progression

- Skill Levels: 1-20 for each skill
- Equipment Quality: Common to Legendary
- Monster Unlocks: 5 sequential monsters
- Permanent Upgrades: Alchemy elixirs
Scaling Mechanics
- Early Game (Levels 1-10): Linear progression, clear upgrades
- Mid Game (Levels 11-15): Diminishing returns, strategic choices
- Late Game (Levels 16-20): Exponential scaling, endgame goals
Long-term Goals
- Max all skills to level 20
- Defeat final monster (Monster 5)
- Craft legendary equipment
- Complete permanent upgrade collection

---

1. MONSTER DESIGN
Monster Progression
| Monster | HP | Damage | Unlock Condition | Special Drops |
|---------|----|--------|------------------|----------------|
| 1 | 100 | 10 | Start | Common gear, basic resources |
| 2 | 250 | 15 | Defeat Monster 1 | Uncommon gear, rare herbs |
| 3 | 500 | 25 | Defeat Monster 2 | Rare gear, epic resources |
| 4 | 1000 | 40 | Defeat Monster 3 | Epic gear, legendary resources |
| 5 | 2500 | 75 | Defeat Monster 4 | Legendary gear, unique components |
Loot System

- Base Drops: Gold, experience for combat skills
- Resource Drops: Skill-specific resources (ores, herbs, wood, hides)
- Equipment Drops: Quality tier based on monster level
- Special Drops: Rare crafting components, unique items

---

1. USER INTERFACE
Layout Structure

- Header: Character stats, current monster, combat status
- Left Panel: Skill tree with action buttons
- Center: Combat visualization, monster information
- Right Panel: Inventory, equipment, resource counts
- Bottom: Action queue, progress bars
Information Display
- Real-time: Action progress, combat damage, resource counts
- Progression: Skill XP bars, level indicators
- Tool Inventory: Durability, efficiency bonuses
- Equipment Stats: Current bonuses, comparison tooltips
Feedback Systems
- Visual: Progress bars, level-up effects, combat animations
- Audio: Action completions, level-ups, monster defeat
- Haptic: Action confirmations (if supported)

---

1. TECHNICAL REQUIREMENTS
Frontend Architecture

- Framework: React 18+ with functional components
- Build Tool: Vite for fast development and builds
- Styling: Tailwind CSS for responsive design
- State Management: React Context + useReducer for game state
- Persistence: LocalStorage for save/load functionality
Performance Considerations
- Optimization: Lazy loading for skill components
- Animation: CSS transitions for smooth feedback
- Memory: Efficient state updates, prevent unnecessary re-renders
- Responsiveness: Mobile-friendly layout, touch controls
Data Structure
gameState = {
  skills: {
    attack: { level: 1, xp: 0, actions: [...] },
    magic: { level: 1, xp: 0, actions: [...] },
    // ... other skills
  },
  resources: {
    gold: 100,
    copperOre: 0,
    // ... other resources
  },
  equipment: {
    weapon: null,
    armor: null,
    // ... other slots
  },
  combat: {
    currentMonster: 1,
    autoAttack: true,
    // ... combat state
  }
}

---

1. MVP SCOPE
Core Features (Must Have)

- ✅ All 9 skills implemented with level 1-20 progression
- ✅ Combat system with 5 monsters
- ✅ Equipment crafting and usage
- ✅ Resource economy (gathering → crafting → usage)
- ✅ Basic UI with skill panels and combat visualization
- ✅ Save/load functionality
Secondary Features (Nice to Have)
- 🔄 Action queuing system
- 🔄 Tool durability and repairs
- 🔄 Shop system for gold purchases
- 🔄 Visual combat animations
- 🔄 Sound effects and audio feedback
Excluded from MVP
- ❌ Multiplayer features
- ❌ Guild or social systems
- ❌ Achievement systems
- ❌ Advanced visual effects
- ❌ Mobile app version

---

1. DEVELOPMENT PHASING
Phase 1: Core Foundation (Week 1-2)

- Game state management system
- Basic skill framework
- Resource tracking
- Save/load functionality
Phase 2: Skill Implementation (Week 3-5)
- Gather skills (Mining, Herbalism, Forestry, Hunting)
- Craft skills (Smithing, Alchemy, Woodworking, Tailoring)
- Combat skills (Attack, Magic)
- Action execution system
Phase 3: Combat & Monsters (Week 6-7)
- Monster combat mechanics
- Auto-attack and magic systems
- 5 monster implementation
- Loot drop system
Phase 4: Equipment & Economy (Week 8)
- Equipment slots and bonuses
- Crafting system integration
- Gold economy
- Shop functionality
Phase 5: UI & Polish (Week 9-10)
- Complete UI implementation
- Progress visualization
- User feedback systems
- Bug fixes and optimization
Phase 6: Testing & Launch (Week 11-12)
- Balance testing and adjustments
- Performance optimization
- Final bug fixes
- Deployment preparation

---

1. SUCCESS METRICS
MVP Success Criteria

- All 9 skills functional with proper XP progression
- Combat system working with all 5 monsters
- Equipment crafting and usage complete
- Resource economy balanced and functional
- Save/load system stable
Player Engagement Targets
- Average session time: 15-30 minutes
- Return player rate: 60%+ within 7 days
- Skill progression: Multiple skills leveled per session
- Monster defeat progression: Regular advancement through monster tiers

---

1. FUTURE EXPANSION
Post-MVP Features

- Advanced equipment customization
- Additional skill trees
- Boss battles with special mechanics
- Achievement and milestone systems
- Visual themes and cosmetic options
Technical Improvements
- Cloud save synchronization
- Mobile app development
- Performance optimization for longer sessions
- Advanced animation systems

---
