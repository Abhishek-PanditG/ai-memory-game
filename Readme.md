# 🧠 Memory Matching Game with AI Player

![AI](https://img.shields.io/badge/Concept-Artificial%20Intelligence-blue) ![JavaScript](https://img.shields.io/badge/Language-JavaScript-yellow) ![Status](https://img.shields.io/badge/Project-Completed-brightgreen) ![Level](https://img.shields.io/badge/Level-Mini%20Project-orange)

---

## 📌 Overview

This project is a **Memory Matching Game (6×6 grid)** built using **JavaScript**, enhanced with **Artificial Intelligence concepts**. Unlike a traditional memory game, this implementation includes an **intelligent AI agent** that:

- 🧠 Learns from past moves
- 💾 Uses memory to make decisions
- 🎯 Applies heuristic strategies
- ⚖️ Balances exploration and exploitation

---

## 🎮 Game Description

### Game Mechanics
- **Board Size:** 6×6 grid containing **36 cards (18 pairs)**
- **Players:** Human vs AI
- **Gameplay:**
  - Each turn, a player flips **two cards**
  - If cards **match** → player scores 1 point and plays again
  - If cards **don't match** → cards flip back face-down
  - Game ends when **all pairs are matched**
  
🏆 **Winner:** The player with the highest score

---

## ⚙️ Features

✅ **Human vs AI Gameplay**
- Turn-based system with clear player indicators
- Real-time score tracking

✅ **Memory-Based AI Decisions**
- AI remembers previously flipped cards
- Uses stored knowledge to find matching pairs

✅ **Turn-Based Scoring System**
- Accurate score calculation
- Bonus turns for successful matches

✅ **Interactive Card Flipping UI**
- Smooth flip animations
- Visual feedback for matches and mismatches

✅ **Hybrid AI Strategy**
- Combines smart decision-making with random exploration
- Adapts based on available information

---

## 🤖 AI Concepts Implemented

### 1. State Space Representation
Each board configuration is treated as a **state** in the problem space.

```
State = {
  cards: [face-up / face-down],
  matched_pairs: number,
  human_score: number,
  ai_score: number
}
```

- **Initial State:** All cards hidden
- **Goal State:** All pairs matched

---

### 2. Intelligent Agent

The AI behaves as a **model-based reflex agent**:

| Component | Description |
|-----------|-------------|
| **Environment** | Game board with 36 cards |
| **Agent** | AI player |
| **Percepts** | Flipped cards and their symbols |
| **Actions** | Selecting two cards to flip |
| **Agent Type** | Model-Based + Reflex Agent |

---

### 3. Memory-Based Learning

The AI maintains a **knowledge base** of seen cards:

```javascript
memory = {
  'A': [3, 12],
  'B': [5, 18],
  'C': [7, 25],
  // ...
}
```

**Decision Logic:**
- If two positions with the same symbol are known → Select that pair
- Else → Explore by flipping a random unknown card

---

### 4. Greedy Heuristic Strategy

The AI uses a **greedy heuristic** approach:

```
IF (known matching pair exists)
    → Select pair (best move)
ELSE
    → Random selection (exploration)
```

**Heuristic Used:** *"Pick known matching pair if available"*

- **Pros:** Fast decision-making, high win rate
- **Cons:** Might miss better long-term strategies

---

### 5. Exploration vs Exploitation

The AI balances two strategies:

| Strategy | Approach | When Used |
|----------|----------|-----------|
| **Exploitation** | Use known pairs from memory | When confident matches exist |
| **Exploration** | Flip unknown cards randomly | When no known pairs available |

This balance improves decision-making efficiency and learning over time.

---

### 6. Game Theory

This is a **two-player competitive game** with:

- **Turn-based moves** → Each player gets a turn
- **Competitive objective** → Maximize own score
- **Rational decision-making** → AI chooses best available move
- **Utility maximization** → Each decision aims to increase score

---

### 7. Knowledge Representation

The AI uses **symbolic representation** for knowledge:

```javascript
memory[symbol] = [position1, position2, ...]
```

- **Type:** Structured, symbolic knowledge
- **Advantage:** Easy lookup and fast decision-making
- **Storage:** O(n) space complexity where n = number of cards seen

---

### 8. Search Problem (Simplified)

The AI solves a simplified search problem:

> *Find all matching pairs efficiently*

Rather than using full **BFS/DFS**, it uses **heuristic-based search**:
- Reduces computation time
- Makes real-time decisions
- Balances accuracy with speed

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **HTML5** | Structure and layout |
| **CSS3** | Styling and animations |
| **JavaScript (ES6+)** | Game logic and AI |
| **No Dependencies** | Pure vanilla JavaScript |

---

## 🚀 How to Run

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No additional installations required

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/memory-ai-game.git
   cd memory-ai-game
   ```

2. **Open the game:**
   - Double-click `index.html` in your file explorer, OR
   - Right-click `index.html` → Open with → Your browser

3. **Play the game:**
   - Click any card to start flipping
   - Try to match pairs against the AI
   - Watch the AI learn your patterns!

---

## 📊 AI Decision Flow

```
┌─────────────────────┐
│    Start AI Turn    │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────────────┐
│ Check Memory for Known Pair │
└──────────┬──────────────────┘
           │
    ┌──────┴──────┐
    │             │
   YES           NO
    │             │
    ▼             ▼
┌────────┐    ┌────────────┐
│Pick    │    │Random Flip │
│Pair    │    │Unknown Card│
└────┬───┘    └─────┬──────┘
     │              │
     └──────┬───────┘
            │
            ▼
    ┌───────────────┐
    │Update Memory  │
    │Check if Match │
    └───────┬───────┘
            │
            ▼
    ┌──────────────────┐
    │Update Score &    │
    │Continue or Switch│
    │to Next Player    │
    └──────────────────┘
```

---

## 🎓 Learning Outcomes

By studying this project, you'll understand:

✅ **Intelligent Agent Fundamentals**
- Percepts, actions, and agent types
- Model-based vs reflex agents

✅ **AI in Game Development**
- How to implement AI opponents
- Decision-making algorithms

✅ **Memory-Based Learning**
- Knowledge representation
- Learning from experience

✅ **Heuristic Decision-Making**
- Greedy algorithms
- Optimization strategies

✅ **Exploration vs Exploitation**
- Balancing discovery and knowledge use
- Real-world applications in AI

✅ **Game Theory Concepts**
- Two-player games
- Competitive vs cooperative strategies
- Utility maximization

---

## 📁 Project Structure

```
memory-ai-game/
│
├── index.html          # Game interface and HTML structure
├── style.css           # Styling and animations
├── script.js           # Game logic and AI implementation
├── README.md           # Project documentation
└── assets/             # Optional: images, fonts
```

---

## 🎮 How to Play

### For Human Players

1. **Click two cards** to flip them
2. **Remember the symbols** you've seen
3. **Find matching pairs** before the AI does
4. **Earn points** for each successful match
5. **Get bonus turns** when you match successfully

### AI Behavior

- AI plays on its turn automatically
- AI remembers cards it has seen
- AI prefers known matches over random flips
- AI adapts strategy based on revealed information

---

## 🔮 Future Enhancements

### Advanced AI Algorithms
- 🔹 **Minimax Algorithm** - Optimal move selection
- 🔹 **Alpha-Beta Pruning** - Optimization technique
- 🔹 **Reinforcement Learning** - Learn from thousands of games

### Game Features
- 🔹 **Difficulty Levels** - Easy, Medium, Hard
- 🔹 **Multiple Themes** - Different card designs
- 🔹 **Sound Effects** - Audio feedback
- 🔹 **Leaderboard** - Track high scores
- 🔹 **Statistics Dashboard** - Win/loss ratio, average turns

### Technical Improvements
- 🔹 **Local Storage** - Save game state
- 🔹 **Multi-player Mode** - Play with friends
- 🔹 **Mobile Optimization** - Touch controls
- 🔹 **AI Difficulty Selector** - Choose AI skill level

---

## 📝 Code Example: AI Memory System

```javascript
class AIMemory {
  constructor() {
    this.memory = {};
  }

  recordCard(position, symbol) {
    if (!this.memory[symbol]) {
      this.memory[symbol] = [];
    }
    this.memory[symbol].push(position);
  }

  findMatchingPair() {
    for (const symbol in this.memory) {
      if (this.memory[symbol].length >= 2) {
        return {
          card1: this.memory[symbol][0],
          card2: this.memory[symbol][1]
        };
      }
    }
    return null;
  }

  makeDecision(unknownCards) {
    const knownPair = this.findMatchingPair();
    
    if (knownPair) {
      return knownPair;  // Exploitation
    } else {
      return this.getRandomCard(unknownCards);  // Exploration
    }
  }
}
```

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📚 References

### Game Development
- Memory Game Theory
- Turn-based Game Design
- UI/UX for Games

---
---
---
---

**Happy Playing! 🎮 May the best player win! 🏆**
