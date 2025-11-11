water jug

1️⃣ Start with both jugs empty (0, 0).
2️⃣ Repeat until one jug has the target amount:
3️⃣ → Fill Jug 1 completely (if not full).
4️⃣ → Fill Jug 2 completely (if not full).
5️⃣ → Empty Jug 1 completely (if needed).
6️⃣ → Empty Jug 2 completely (if needed).
7️⃣ → Pour water from Jug 1 → Jug 2 until one is full or the other is empty.
8️⃣ → Pour water from Jug 2 → Jug 1 until one is full or the other is empty.
9️⃣ Mark each new state (Jug 1, Jug 2) as visited to avoid repetition.
🔟 When either jug equals the target, stop and print the path.



n queens

1️⃣ Start with an empty chessboard of size N×N.
2️⃣ Place a queen in the leftmost column (starting from column 0).
3️⃣ For each column, try placing a queen in every row one by one.
4️⃣ Before placing, check if the position is safe (no queen in same row, upper-left, or lower-left diagonal).
5️⃣ If safe, place the queen and move to the next column (recursively).
6️⃣ If placing in the next column fails, remove (backtrack) the previous queen and try the next row.
7️⃣ Repeat until all N queens are placed safely on the board.
8️⃣ Each valid arrangement is one solution — print or store it.
9️⃣ After exploring all possibilities, display the total number of solutions.



travelling sales man

1️⃣ List all possible routes visiting each city exactly once and returning to the start.
2️⃣ For each route, calculate the total travel cost using the given distance matrix.
3️⃣ Compare all route costs and record the one with the minimum total distance.
4️⃣ Display the shortest path and its minimum cost.



missionarties

1️⃣ Start with 3 missionaries (M) and 3 cannibals (C) on the left bank.
2️⃣ Repeat until all are safely on the right bank:
3️⃣ → Choose 1 or 2 people (missionaries/cannibals) to move across in the boat.
4️⃣ → Update counts on both sides after each crossing.
5️⃣ → Check if on either bank cannibals outnumber missionaries → if yes, game over (missionaries get eaten!).
6️⃣ → Continue moving back and forth, keeping both sides safe after every move.
7️⃣ Stop when all 6 people are on the right bank — you win!
8️⃣ Count and display the total number of moves made.



AO

1️⃣ Start with the given start node and initial heuristic values.
2️⃣ Expand the current node (n) to generate all its AND and OR child combinations.
3️⃣ For each combination, calculate total cost = heuristic(child) + 1 for each link.
4️⃣ Select the combination (AND/OR) with the minimum total cost as the best option.
5️⃣ Update the node’s heuristic value (h[n]) to this best cost.
6️⃣ Recursively apply AO* to each child node of the selected best combination.
7️⃣ Mark the node as solved when all its best children are solved.
8️⃣ Repeat until the start node is solved — its heuristic becomes the optimal cost.



A

1️⃣ Initialize all nodes with infinite cost (g), except the start node (g=0).
2️⃣ Use a list (Open set) to track nodes to explore.
3️⃣ Pick the node with the smallest total cost f(n) = g(n) + h(n).
4️⃣ If it’s the goal node, stop — the optimal path is found.
5️⃣ For each neighbor, calculate new g = current g + edge cost.
6️⃣ If this g is smaller than the stored one, update g and parent link.
7️⃣ Add neighbors to the Open set if not already explored.
8️⃣ Repeat until the goal is reached or Open set is empty.



wumpus

1️⃣ Create a 4×4 grid and randomly place the Wumpus, Gold, and Pits (not in the starting cell).
2️⃣ Add clues: mark “Breeze” around each Pit and “Stench” around the Wumpus.
3️⃣ Start the agent at (0,0) — the safe cell.
4️⃣ At each step, display the agent’s current percept (Breeze, Stench, Glitter, or Safe).
5️⃣ Take player input (‘up’, ‘down’, ‘left’, ‘right’) and move accordingly.
6️⃣ If the agent moves outside the grid, show “Hit Wall!”
7️⃣ If the agent reaches Gold, display “You Win!”
8️⃣ If the agent falls into a Pit or meets the Wumpus, display “Game Over!”.
9️⃣ Reveal the full world grid at the end of the game.
