🧠 Memory Matching Game with AI Player
📌 Project Overview

This project is a Memory Matching Game (6×6 grid) developed as part of an Artificial Intelligence mini-project. The game involves a human player competing against an AI agent to find matching card pairs.

The AI player is designed using core AI concepts such as model-based learning, heuristic decision-making, and exploration vs exploitation, making the project more than just a simple game.

🎮 Game Description
The board consists of a 6×6 grid (36 cards).
Each card has a hidden symbol.
Players take turns flipping two cards at a time:
If they match → player scores a point and gets another turn.
If not → cards flip back.
The game ends when all pairs are matched.
The player with the highest score wins.
🤖 AI Implementation
1. Intelligent Agent

The AI acts as an agent in the environment.

Environment: Game board
Agent: AI player
Percepts: Flipped cards
Actions: Selecting two cards

👉 Type:

Reflex + Model-Based Agent
2. Model-Based Learning (Memory System)

The AI stores previously seen cards and uses this knowledge for future decisions.

memory = {
  'A': [2, 15],
  'B': [7]
}
If AI knows both positions of a symbol → it selects them.
Otherwise → explores randomly.

👉 This demonstrates:

Learning from past observations
Knowledge reuse
3. State Space Representation

Each configuration of the board is treated as a state.

State: Arrangement of cards (face up/down + matched)
Initial State: All cards hidden
Goal State: All pairs matched

👉 This maps the problem to a state space search problem.

4. Greedy Heuristic Strategy

The AI follows a greedy approach:

If a known pair exists → choose it (optimal move)
Else → choose random cards

👉 Heuristic used:

“Pick known matching pair if available”

5. Exploration vs Exploitation

The AI balances:

Exploitation: Using memory to pick known pairs
Exploration: Flipping unknown cards randomly

👉 This is a fundamental AI concept used in:

Reinforcement Learning
Decision-making systems
6. Game Theory Concepts

The game models a 2-player competitive environment:

Player vs AI
Turn-based strategy
Score maximization

👉 Concepts used:

Rational decision making
Utility maximization
7. Knowledge Representation

The AI stores knowledge in a structured format:

memory[symbol] = [positions]

👉 This is:

Symbolic representation
Structured knowledge storage
8. Search Problem (Simplified)

The AI is solving:

“Find all matching pairs with maximum efficiency”

Though not using full algorithms like BFS/DFS, it still behaves like a:

Heuristic-based search system
🛠️ Technologies Used
Frontend: HTML, CSS, JavaScript
Logic: JavaScript (AI + Game Logic)
🚀 How to Run the Project
Download or clone the repository
Open the project folder
Run the index.html file in a browser
🎯 Key Learning Outcomes
Understanding of intelligent agents
Application of AI in games
Practical implementation of:
Model-based learning
Heuristic decision-making
Exploration vs exploitation
🧪 Future Improvements
Implement Minimax Algorithm for smarter AI
Add Alpha-Beta Pruning for optimization
Use Reinforcement Learning for adaptive AI
Add difficulty levels
🗣️ Viva Explanation (Short Answer)

“This project implements a model-based intelligent agent that uses memory to store previously seen card positions. The AI applies a greedy heuristic by selecting known pairs when available, otherwise exploring randomly. It also demonstrates concepts like state space representation, game theory, and exploration vs exploitation in a turn-based environment.”