# Creat-AR - Game Design Document

## Game Overview

**Game Title:** Creat-AR

**Genre:** Roguelike creature collection and adventure game with base management  
**Platform:** Desktop (Java), with potential for cross-platform mobile AR implementation  
**Target Audience:** Casual gamers ages 8+  
**Development Team:** 3 members  

## Concept Statement

Creat-AR is a roguelike creature collecting and battling game where players hatch, raise, 
and adventure with elemental creatures. Each creature has unique procedurally-generated appearances created 
from mix-and-match body parts. Players embark on branching-path adventures of increasing difficulty, collecting 
temporary upgrade cards during each run while their creatures gain permanent passive abilities as they level up. 
Between adventures, players manage their home base, building facilities to care for creatures, grow food, and 
enhance their collection.

## Key Features

- Procedurally generated voxel-art creatures with mix-and-match body parts
- Five elemental affinities affecting aesthetics and starting attributes
- Rare "Rainbow" variant creatures with enhanced stats
- Home base management with building upgrades and creature care
- Slay the Spire-inspired branching path adventures
- Progressive difficulty tiers that unlock as you defeat bosses
- Temporary upgrade cards with pathway system affecting future choices
- Permanent passive abilities gained every 10 levels
- Creature recovery system
- Sanctuary rooms to collect new creature eggs

## Core Game Mechanics

### Creature Attributes

1. **HP (Health Points)**: How much damage a creature can withstand
2. **Energy**: Resource for using abilities during battle
3. **Defense**: Reduces incoming damage
4. **Strength**: Determines attack damage
5. **Speed**: Affects dodge chance (avoiding attacks)
6. **Luck**: Affects critical hit chance and item find quality

### Elemental Affinities

Each creature belongs to one of five elemental types, affecting appearance and stat growth:

- **Earth**: High HP and Defense, low Speed
- **Fire**: High Strength, lower HP
- **Water**: Balanced growth across all attributes
- **Ice**: High HP and Defense, low Strength
- **Electricity**: High Speed and Energy, lower HP

### Rainbow Variant

Ultra-rare creatures (1% chance when hatching) with:
- +15% to all base stats
- Additional card slot during adventures
- Extra passive ability selection at level milestones
- 10% more experience gain

## Base Management System

### Core Resources

1. **Food**
   - Grown in garden plots on your base
   - Single food type used for all creatures
   - Used for feeding creatures to maintain hunger levels
   - Keeps creatures happy when hunger is above threshold

2. **Materials** (Wood, Stone, Crystal, Metal)
   - Primary building resources for structures
   - Found exclusively during adventures
   - Different buildings require specific combinations

3. **Gold**
   - Universal currency for purchases
   - Earned primarily from adventures
   - Used for blueprints and special items
   - Can speed up certain processes

### Key Buildings

1. **Garden Plot** (Starting Building)
   - Basic food production facility
   - Expandable with multiple plots
   - Single crop type for consistent food production
   - Simple growth cycle with consistent yields

2. **Elemental Habitats**
   - Specialized housing matching creature elements
   - Earth: Crystal Cave with moss beds
   - Fire: Lava pool with warm stone resting areas
   - Water: Gentle pool with underwater resting spots
   - Ice: Frost cave with cool crystal formations
   - Electricity: Conductivity chamber with energy fields
   - Provides 15% stat bonus to matching elemental creatures
   - Reduces recovery time by 25% for matching elements
   - Three upgrade tiers with increasing benefits

3. **Recovery Center**
   - Medical facility for wounded creatures
   - Reduces recovery time by 50%
   - Can treat multiple creatures based on upgrade level
   - Uses food resources to speed healing process
   - Three upgrade tiers increasing capacity and efficiency

4. **Training Grounds**
   - Passive XP gain for housed creatures
   - Safe practice battle simulations
   - Specialized training stations for specific attributes
   - Three upgrade tiers with better training effectiveness
   - Optional usage - no penalties for not training

5. **Incubation Chamber**
   - Enhanced egg hatching facility
   - Uses crystals to power incubation process
   - Increases rainbow variant chances (up to 3%)
   - Reduces hatching time by up to 50%

6. **Home Sanctuary**
   - Attracts wild creature eggs
   - Random elemental type for eggs
   - Upgrade to increase egg frequency
   - Uses food as an attraction resource

### Creature Care Systems

1. **Happiness System**
   - Creatures have happiness level from 0-100%
   - Below 50%: Reduced performance in adventures
   - 50-75%: Normal performance
   - 75-100%: Enhanced performance (up to +10% to all stats)
   - Affected by:
     - Appropriate habitat (+1% per hour)
     - Hunger above threshold (+5% base happiness)
     - Recent adventures (+10% for successful completion)
     - Recovery from injuries (-20%, gradually improves)

2. **Feeding System**
   - Simple hunger meter system (0-100%)
   - As long as hunger stays above 50%, no happiness penalties
   - Single food type works for all creatures
   - No feeding schedule required - just maintain threshold
   - Feeding fills hunger bar based on food quantity

3. **Training System**
   - Completely optional system
   - Use for passive XP gain when not adventuring
   - No penalties for not using training facilities
   - Focused training for specific attributes

### Building Progression

1. **Tiered Upgrades**
   - Each building has three upgrade levels
   - Tier 1: Basic functionality
   - Tier 2: Enhanced capacity and efficiency (+50%)
   - Tier 3: Maximum benefits (+100%) and special features
   - Visual improvements with each tier
   - Increasing material costs for higher tiers

2. **Fixed Building Locations**
   - Each building has a predetermined location on the base
   - No need for placement decisions
   - Clear progression path for base development

## Adventure System

- Four difficulty tiers: Beginner, Medium, Hard, Veteran
- Each tier features progressively larger maps and stronger enemies
- Branching paths with player choice of route
- Node types include: Battles, Elite Battles, Sanctuaries, Rest Sites, Mystery Nodes, Treasure Nodes, and Boss Nodes
- Defeat a tier's boss to unlock the next difficulty level

### Creature Recovery System

When a creature is defeated in battle:
- The creature enters a "wounded" state
- The current adventure ends immediately
- Creature requires recovery time before adventuring again:
  - Beginner maps: 10-15 minutes real time
  - Medium maps: 30-45 minutes real time
  - Hard maps: 1-2 hours in real time
  - Veteran maps: 3-4 hours in real time
- Recovery time can be reduced through:
  - Recovery Center placement (50% reduction)
  - Elemental Habitat matching (25% additional reduction)
  - Happiness level (up to 15% additional reduction)
  - Food availability (basic healing support)

### Sanctuary System

- Special nodes where players can obtain new eggs
- First room visited is always a sanctuary if player has no eggs/creatures
- Higher difficulty adventures offer rarer or specialized eggs

### Battle System

#### Basic Moves (Available to All Creatures)

These fundamental moves are available to every creature regardless of element or level:

1. **Basic Attack**
   - Simple damage based on creature Strength
   - No energy cost
   - Can critical hit based on Luck

2. **Block**
   - Increases Defense by 50% until next turn
   - Reduces damage from next attack
   - Energy cost: 10

3. **Focus**
   - Skip attack to restore 15 Energy
   - Increases critical hit chance by 10% on next turn
   - No energy cost

4. **Elemental Attack** (Signature Special Attack)
   - Unique special attack based on creature's elemental affinity
   - Higher damage or special effects
   - Higher energy cost

#### Elemental Signature Attacks

Each creature starts with one signature special attack based on its elemental affinity:

- **Earth - Boulder Crush**: Deal damage equal to 140% of Strength and gain temporary Defense equal to 30% of damage dealt (Energy cost: 20)
- **Fire - Inferno Strike**: Deal damage equal to 180% of Strength with a 25% higher critical chance (Energy cost: 25)
- **Water - Tidal Surge**: Deal damage equal to 160% of Strength and restore 10 Energy (Energy cost: 20)
- **Ice - Glacial Spike**: Deal damage equal to 150% of Strength and reduce enemy's Strength by 15% for 2 turns (Energy cost: 25)
- **Electricity - Lightning Bolt**: Deal damage equal to 170% of Strength with guaranteed critical hit on enemies below 50% HP (Energy cost: 25)

## Progression Systems

### Permanent Upgrades (Every 10 Levels)

Creatures can reach a maximum level of 100, gaining a permanent upgrade every 10 levels. At each milestone, players select one upgrade from three options:

**Level 10 Options**
- Vitality I (HP +10%)
- Power I (Strength +10%)
- Fortification I (Defense +10%)

**Level 20 Options**
- Energy Flow I (Energy regen +2/turn)
- Lucky Strike I (Critical chance +5%)
- Swift Movement I (Dodge chance +5%)

**Level 30-90 Options**
- Progressive tiers of permanent stat and ability enhancements
- Increased effects at higher tiers (I, II, III)

**Level 100 Options (Final Tier)**
- Ultimate Vitality (HP +30%, heal 5% each turn)
- Ultimate Power (Strength +30%, chance for free Basic Attacks)
- Ultimate Defense (Defense +30%, all damage -10%)

### Temporary Card System

During adventures, creatures collect temporary upgrade cards after battles that last only for the current run:

**Rarity Tiers:**
- Common (60% chance)
- Uncommon (30% chance)
- Rare (9% chance)
- Epic (1% chance)

Higher rarity cards provide stronger effects, with Epics potentially changing the whole strategy for a run.

### Card Pathway System

Cards are organized into five categories that create distinct build pathways:

1. **Offensive** - Focus on attack damage and critical hits
2. **Defensive** - Focus on damage reduction and survivability
3. **Utility** - Focus on energy management and versatility
4. **Speed** - Focus on dodge chance and action frequency
5. **Sustain** - Focus on healing and resource recovery

When a player selects a card, it influences future card offerings:
- Cards from the same category become 25% more likely to appear
- Cards from opposing categories become 25% less likely to appear
- After selecting 3 cards from the same category, that pathway becomes "committed" with stronger effects

**Category Relationships:**
- **Offensive** opposes **Defensive**
- **Utility** opposes **Speed**
- **Sustain** has no direct opposite but becomes less compatible with committed pathways

## Adventure-Base Integration

### Pre-Adventure Preparation
- Ensure creatures have hunger meters above threshold
- Select well-rested creatures for optimal performance
- Set up recovery facilities for potential injuries

### Post-Adventure Benefits
- Returning with materials for base improvements
- Gold rewards for successful completion
- Occasional egg finds as rare rewards

### Home Sanctuary System
- Build and upgrade Sanctuary to attract wild eggs
- Use food as bait to attract creatures
- Daily chance to find new eggs (10-30% based on level)
- Random elemental types for eggs

## User Interface

### Main Menu / Home Base
- Creature collection display with status indicators (available, wounded, recovering)
- Recovery timer displays for wounded creatures
- Adventure difficulty selection
- Base management options
- Building upgrade interface
- Collection journal
- Settings

### Base Management Screen
- Overview of all buildings and their status
- Resource counts and production rates
- Creature assignment interface
- Upgrade options for buildings

### Recovery Care Screen
- Wounded creature visualization
- Recovery progress bar
- Care action buttons
- Estimated time to full recovery
- Status effects from wounds

### Adventure Map Screen
- Visual map with branching paths
- Node icons showing encounter types
- Current location and path options
- Creature status summary
- Pathway commitment indicators

### Battle Screen
- Creature visualization
- Health and Energy bars
- Action selection
- Card/ability use interface
- Battle log

### Card Selection Screen
- Three cards displayed after battles
- Card category indicators and pathway information
- Card details and effects
- Selection confirmation
- Visual indication of pathway influence on card selection

## Technical Implementation

### Data Structures

1. **Creature Generation**
   - Procedural combination of body parts
   - Element-based appearance variations
   - Attribute distribution based on element type
   - Rainbow variant special properties

2. **Branching Path Map**
   - Directed graph structure for map representation
   - Node-type distribution based on difficulty tier
   - Path navigation and progression tracking

3. **Card Pathway System**
   - Category tracking and commitment thresholds
   - Weighting system for future card offerings
   - Opposing pathway limitations

4. **Base Management System**
   - Building upgrade tracking
   - Resource production and consumption calculations
   - Creature happiness and hunger simulation
   - Recovery time calculations

## Art Style and Assets

- Voxel-style creatures with mix-and-match body parts
- 5-7 head variations per element
- 3-5 body variations per element
- 4-6 limb variations per element
- 3-4 tail/accessory variations per element
- Consistent connection points for proper assembly
- Pixel art UI elements
- Elemental-themed buildings for the home base
- Elemental-themed environments for different map areas

## Team Roles

- **Project Lead**: Miles - Architecture design, core Java implementation, art asset creation, soundFX, music, game mechanics, data structures, backend systems
- **UI/UX Developer**: Brisa - Interface design, user experience, visual elements, game mechanics, data structures, backend systems
- **Technical Developer**: Emilio - Technical implementation, game mechanics implementation, data structures, backend systems

## Technical Constraints

- Developed in Java 17+
- Object-oriented programming principles
- Multiple data structures implementation
- GitHub version control
- JavaFX for UI (initial implementation)
- Unity + AR Foundation 

## Post-MVP Features (Future Development)

- Online leaderboards
- Daily challenges
- Expanded egg collection with special events
- Social features for sharing creatures
- Advanced animation system
- Additional elements and creature types
- Story mode with narrative elements
