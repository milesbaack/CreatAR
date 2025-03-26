# 🐉 Creat(AR)

A roguelike creature collection and adventure game with base management, developed in Java for CSIS-294 Object-Oriented Design and Programming.

## 📋 Project Overview

Creature Keeper is a roguelike monster-raising game where players hatch, raise, and battle with elemental creatures. Each creature has a unique procedurally-generated appearance created from mix-and-match body parts. Players embark on branching-path adventures, collecting temporary upgrade cards while creatures gain permanent passive abilities.

Between adventures, players manage their home base, build facilities, grow food, and care for their creatures. The game features a recovery system where defeated creatures need time to heal, encouraging players to develop a diverse collection.

## 🏆 M.V.P.

The minimum-viable-product will be a desktop version of the game using JavaFX, with plans to expand into a mobile augmented realty (AR) application using Unity for cross-platform compatibility. Unity supports Java through plug-ins and has built in AR frameworks for (relatively) simple mobile deployment. We just need to give Unity an executable JAR file... (it's more complicated than that but I am still figuring out all the specifics)

## 🌟 Key Features

- **Procedurally Generated Creatures**: Mix-and-matched body parts with five elemental affinities color-schemes and effects (Earth, Fire, Water, Ice, Electricity)
- **Roguelike Adventures**: Slay the Spire-inspired branching paths with four difficulty tiers
- **Base Management**: Six key buildings to develop, upgrade, and manage your creature collection
- **Card System**: Temporary upgrade cards with five pathway categories (Offensive, Defensive, Utility, Speed, Sustain)
- **Permanent Progression**: Milestone abilities every 10 levels up to level 100
- **Recovery System**: Wounded creatures require time to heal based on adventure difficulty
- **Rainbow Variants**: Ultra-rare creatures (1% chance) with enhanced stats and abilities

## 🔄 Game Loop

1. **Hatch** creatures from eggs found in adventures and the home sanctuary
2. **Care** for creatures at your home base to maintain hunger levels and happiness
3. **Improve** your base with materials (Wood, Stone, Crystal, Metal) gathered from adventures
4. **Adventure** through procedurally generated maps with branching paths
5. **Battle** enemies using Basic Attacks, Block, Focus, and Elemental Attacks
6. **Collect** temporary upgrade cards that influence future card offerings
7. **Recover** wounded creatures through the recovery system (10 min - 4 hours based on difficulty)
8. **Repeat** with new creatures to build a diverse collection

## 🏗️ Architecture

The project follows object-oriented design principles with a clear separation of concerns:

- **Core Domain Model**: Creatures, elements, attributes (HP, Energy, Defense, Strength, Speed, Luck), abilities
- **Adventure System**: Maps, nodes, battles, card pathways
- **Base Management**: Buildings (Garden Plot, Habitats, Recovery Center, Training Grounds, Incubation Chamber, Sanctuary), resources, creature care
- **Battle System**: Turn-based combat, elemental attacks, card effects
- **UI Layer**: JavaFX implementation for game interface

## 📊 Data Structures

- **Directed Graphs**: Adventure map generation with branching paths
- **Hash Maps**: Entity lookups, building management, creature collection
- **Queues**: Battle turn management, recovery system
- **Lists/ArrayLists**: Card collections, creature attributes
- **Custom Structures**: Card pathway weighting system, happiness and hunger systems

## 💻 Technology Stack

- **Language**: Java 17+
- **UI Framework**: JavaFX
- **Version Control**: Git/GitHub
- **Potential Future**: Unity with AR Foundation for mobile

## 🗓️ Development Timeline

### Phase 1: Core Systems (March 25 - April 21)
- [x] Project setup and repository creation
- [ ] Core class structure and UML diagrams
- [ ] Creature generation system with mix-and-match body parts
- [ ] Elemental affinities and attribute systems
- [ ] Basic combat calculations for the four core moves
- [ ] Core UI foundation
- [ ] Rainbow variant implementation

### Phase 2: Adventure Mode (April 22 - May 5)
- [ ] Branching path map generation algorithm
- [ ] Battle system with elemental signature attacks
- [ ] Card pathway system with five categories
- [ ] Permanent upgrade system for level milestones
- [ ] Node types (Battles, Elite Battles, Sanctuaries, etc.)
- [ ] Recovery system implementation

### Phase 3: Base Management (May 6 - May 19)
- [ ] Building implementation (all six structures)
- [ ] Resource management (Food, Materials, Gold)
- [ ] Creature care systems (Happiness, Hunger)
- [ ] Building upgrade mechanics
- [ ] Home sanctuary for egg collection
- [ ] Creature artwork and animation foundations

### Phase 4: Polish & Integration (May 20 - May 29)
- [ ] System integration and balancing
- [ ] UI polish and refinement
- [ ] Bug fixes and performance optimization
- [ ] Final testing and documentation
- [ ] Optional AR implementation if time permits

## 👥 Team Members

- **Project Lead**: Miles - Architecture design, core Java implementation, art asset creation, soundFX, music, game mechanics, data structures, backend systems
- **UI/UX Developer**: Brisa - Interface design, user experience, visual elements, game mechanics, data structures, backend systems
- **Technical Developer**: Emilio - Technical implementation, game mechanics implementation, data structures, backend systems

## 🔍 Getting Started

### Prerequisites
- Java JDK 17 or higher
- IDE (VSCode)
- Github

### Setup Instructions
1. Clone the repository *(I don't think this will work yet)*
```bash
git clone https://github.com/milesbaack/creatAR.git
```

2. Import as Maven project in your IDE

3. Run the main application
```bash
mvn javafx:run
```

## 📁 Project Structure

```
creature-keeper/
├── src/
│   ├── main/
│   │   ├── java/com/creaturekeeper/
│   │   │   ├── core/                 # Core domain model
│   │   │   │   ├── creature/         # Creature classes and generation
│   │   │   │   ├── element/          # Elemental types and effects
│   │   │   │   └── attributes/       # Stats and calculations
│   │   │   ├── adventure/            # Adventure system
│   │   │   │   ├── map/              # Map generation
│   │   │   │   ├── nodes/            # Node types
│   │   │   │   └── cards/            # Card pathway system
│   │   │   ├── base/                 # Base management system
│   │   │   │   ├── buildings/        # All six building types
│   │   │   │   ├── resources/        # Resource management
│   │   │   │   └── care/             # Creature care system
│   │   │   ├── battle/               # Battle mechanics
│   │   │   │   ├── moves/            # Basic and elemental attacks
│   │   │   │   ├── effects/          # Status effects
│   │   │   │   └── recovery/         # Recovery system
│   │   │   ├── ui/                   # JavaFX UI components
│   │   │   │   ├── screens/          # Main game screens
│   │   │   │   ├── components/       # Reusable UI elements
│   │   │   │   └── animations/       # Visual effects
│   │   │   └── util/                 # Utility classes
│   │   └── resources/
│   │       ├── assets/               # Images and art assets
│   │       │   ├── creatures/        # Creature body parts
│   │       │   ├── buildings/        # Building graphics
│   │       │   └── ui/               # UI elements
│   │       ├── css/                  # Style sheets
│   │       └── fxml/                 # JavaFX layouts
│   └── test/                         # Unit tests
├── .gitignore
├── pom.xml                           # Maven configuration
└── README.md
```

## 📝 Documentation

- [Game Design Document](CreatAR/GameDesignDocument.md)
- [UML Diagrams](docs/UML.md)
- [Meeting Notes](docs/meetings/)

## 🤝 Contributing

1. Create a feature branch from `develop`
2. Implement your changes
3. Submit a pull request
4. Get code review from team members
5. Merge once approved


## 🔒 License

This project is private and for academic purposes only. I plan on releasing this game to the Apple App Store, and Google Play Store for free once the AR component is completed, but that is probably out of scope for this project. All possible future proceeds would be shared equitably based off the amount of work put in by each team member. This would be all of our first *real* project though, so let's not even worry about making any money off it for now. Let us instead focus on actually being able to complete it on time LOL... we have a lot of work to do...

---

*Last updated: March 25, 2025*
