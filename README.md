# SkillIssue.exe — An Adaptive AI Dungeon Crawler 🎮

**What if the final boss knew how you played — and used that knowledge against you?**

SkillIssue.exe is a 2D action game built with **Godot and GDScript**, where an adaptive AI Director observes player behavior, identifies gameplay patterns, and dynamically changes the challenge. From punishing predictable dodges to exploiting repetitive attack patterns, the game turns your own habits into your biggest weakness.

Inspired by the idea of an AI game director, SkillIssue.exe blends action combat, behavioral telemetry, dynamic difficulty, and psychological mind games into one experience.

> **You don't just fight the boss. You fight the version of yourself it has learned to counter.**

## 🧠 Core Features

### 🤖 Adaptive AI Director

A persistent AI Director tracks how you play and uses behavioral signals to influence the dungeon and prepare the final boss.

- **Behavioral tracking:** Monitors dodge direction, attack rhythm, aggression, retreating, and combat tempo.
- **Dynamic difficulty:** Adjusts enemy pressure and environmental hazards based on observed behavior.
- **Personalized boss encounters:** The final boss can exploit predictable movement and attack patterns instead of relying solely on fixed attack sequences.
- **Real-time feedback:** An in-game telemetry HUD exposes behavioral metrics and adaptation signals.

### ⚔️ Dynamic Combat & Dungeon Mechanics

The dungeon evolves as you progress, making repeated strategies increasingly risky.

- **Adaptive enemy waves:** Aggressive play can trigger additional reinforcements.
- **Environmental manipulation:** Slippery ice and other hazards interfere with predictable movement.
- **Directional counterplay:** Repeatedly dodging in the same direction can lead to restriction of movement in that direction.
- **Progressive encounters:** Fight through multiple rooms before reaching the adaptive boss arena.

### 💀 Psychological Warfare

The game embraces the *skill issue* meme by making the experience feel personal.

- Contextual boss commentary and trash talk.
- Gameplay modifiers that punish predictable habits.
- A focus on subverting player expectations rather than simply increasing enemy health.

### 📊 Behavioral Telemetry

The adaptation system uses gameplay observations to build a lightweight model of player behavior.

| Behavior observed               | Possible response                           |
| ------------------------------- | ------------------------------------------- |
| Excessive aggression            | Additional enemies to counter               |
| Prolonged retreating            | Disables Dashing of movement in a direction |
| Highly repetitive attack timing | Gives Debuffs                               |

These examples describe the intended adaptation logic; exact triggers and responses depend on the implemented game configuration.

## 🛠️ Tech Stack

- **Game engine:** Godot Engine 4.x
- **Programming language:** GDScript
- **Game architecture:** Event-driven behavioral tracking and a persistent AI Director
- **Gameplay systems:** 2D combat, enemy AI, room transitions, dynamic difficulty
- **Visual effects:** Custom 2D assets, animation, and shader-based effects
- **AI dialogue:** Contextual dialogue generation and LLM integration where configured

## 🎮 Controls

| Action                       | Controls                                 |
| ---------------------------- | ---------------------------------------- |
| Move                         | `W` `A` `S` `D` or Arrow Keys            |
| Attack                       | Left Mouse Button / `J` / `Z` / `Space`  |
| Dash / Dodge                 | Right Mouse Button / `Shift` / `C` / `K` |
| Toggle AI Director HUD       | `F1`                                     |
| Skip to next room *(debug)*  | `F2`                                     |
| Defeat all enemies *(debug)* | `F3`                                     |
| Restart run                  | `R`                                      |

*Some controls and debug shortcuts may depend on the current project configuration.*

## 🚀 Getting Started

### Prerequisites

- [Godot Engine](https://godotengine.org/download/) — use the version specified by the project setup guide.
- Git, if you want to clone the repository.

### Run locally

1. Clone the repository:

   ```bash
   git clone https://github.com/aarkie24/Skillissue.exe.git
   ```

2. Navigate into the project:

   ```bash
   cd Skillissue.exe
   ```

3. Open Godot and import the project by selecting the `project.godot` file.

4. Let Godot import the project assets and dependencies.

5. Run the configured main scene using **F6** for the current scene or **F5** for the project’s main scene.

**Note:** Consult [`SETUP.md`](SETUP.md) if your checkout requires additional scene assembly or configuration.

## 🏗️ How It Works

At a high level, the game follows a behavioral feedback loop:

```text
Player Actions
      │
      ▼
Behavior Tracking
      │
      ▼
AI Director
      │
      ├──► Analyze gameplay patterns
      │
      ├──► Adjust dungeon difficulty
      │
      └──► Prepare boss counter-strategies
                    │
                    ▼
           New Gameplay Challenge
                    │
                    └────► Repeat
```

The core idea is to make difficulty **responsive to player behavior**, rather than relying entirely on predetermined difficulty settings.

The player becomes part of the game's evolving challenge: every repeated action provides another opportunity for the Director to adapt.

## 📁 Project Structure

```text
Skillissue.exe/
├── assets/           # Game assets
├── autoload/         # Persistent systems, including the AI Director
├── scenes/           # Game scenes and encounter layouts
├── scripts/          # Gameplay, combat, and AI logic
├── player_frames/    # Player animation assets
├── dash_frames_raw/  # Dash animation assets
├── project.godot     # Godot project configuration
├── SETUP.md          # Setup and configuration guide
└── README.md
```

## 🎯 Project Goals

SkillIssue.exe explores a simple but interesting game-design question:

**Can a game create a more personal and engaging challenge by learning how its player behaves?**

The project brings together several engineering ideas:

- Modeling player behavior from gameplay events.
- Translating behavioral signals into actionable game-state changes.
- Designing an adaptive difficulty system.
- Connecting combat AI, environmental hazards, and encounter progression.
- Using contextual dialogue and presentation to reinforce the feeling that the game is reacting to the player.

## 🔮 Future Possibilities

Potential areas for further development include:

- More nuanced player-behavior classification.
- Additional adaptive boss phases and counter-strategies.
- Better balancing of difficulty adjustments.
- Expanded contextual dialogue and personality.
- Improved visual feedback explaining how the Director responds to player behavior.

## 👨‍💻 About

Built as a game-development experiment around **adaptive AI, player modeling, and dynamic gameplay**.

The objective isn't simply to make the game harder. It's to make the game harder *in the specific ways that challenge you*.

If the boss keeps countering your moves, maybe it isn't cheating.

Maybe you really do have a skill issue.

---

**Made with Godot. Fueled by questionable decisions and adaptive AI.**
