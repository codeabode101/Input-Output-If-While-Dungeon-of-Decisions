### 🕹️ 5-Day Python Project: "Dungeon of Decisions"

---

#### ✏️ **Day 1: Create Your Game World**

🎯 **Objective**: Set up a playable loop with your character, room, and basic controls
🧠 **Concepts**: variables, `print()`, `input()`, while loops
🕒 **Estimated time**: 45–60 minutes

🛠 **Instructions**:

1. Create three variables:

   * `player_name` → ask the player to enter their name using `input()`
   * `current_room` → start in "Entrance"
   * `game_over` → set this to `False` (you’ll use it to control your game loop)

2. Print a welcome message like:
   `"Welcome, [player_name], to the Dungeon of Decisions!"`

3. Use a `while not game_over:` loop to start your game.

4. Inside the loop:

   * Print: `"You are in the [current_room]. What do you want to do?"`
   * Use `input()` to get a command like "go north" or "open door"
   * For now, only check if the user typed `"quit"` and if so:

     * Set `game_over = True`
     * Print: `"Thanks for playing, [player_name]!"`

💡 **Challenge Extension**:
Try adding a second room: if the user types `"go north"` from the Entrance, change `current_room` to "Hallway" and print a special message.

✅ **Submission**: Share your Python file with your CodeAbode mentor.

---

#### ✏️ **Day 2: Add Choices & Outcomes**

🎯 **Objective**: Add `if` statements to make real decisions matter
🧠 **Concepts**: `if/else`, `input()`, variables
🕒 **Estimated time**: 45–60 minutes

🛠 **Instructions**:

1. Add at least **two rooms**: "Entrance" and "Hallway"

2. In the game loop, check what room you're in with an `if`:

   * If in "Entrance":

     * Ask: `"There's a door to the north. Type 'go north' to continue."`
     * If user types "go north", change room to "Hallway"

   * If in "Hallway":

     * Ask: `"A spooky chest is here. Type 'open chest' or 'go back'."`
     * If "open chest": print something funny or spooky!
     * If "go back": return to "Entrance"

3. Add a `quit` option from any room.

💡 **Challenge Extension**:
Hide a secret code inside the chest and print:
`"You found a glowing crystal with the code: ZAP123"`

✅ **Submission**: Update your game file and send it in.

---

#### ✏️ **Day 3: Add Health & Simple Battles**

🎯 **Objective**: Add a basic health system and simple enemy logic
🧠 **Concepts**: variables, `if`, `-=`, game loops
🕒 **Estimated time**: 60–75 minutes

🛠 **Instructions**:

1. Add a new variable at the top: `health = 10`

2. In the Hallway, if the player types `"open chest"`:

   * Print `"A skeleton jumps out!"`
   * Ask: `"Do you fight or run?"`
   * If "fight": subtract 3 from `health` and print:

     * `"You win, but lose some health! Current health: [health]"`
   * If "run": return to Entrance

3. If `health <= 0` at any time, print:

   * `"You faint and the game ends!"`, then set `game_over = True`

💡 **Challenge Extension**:
Let the player *gain* health if they find a healing potion (e.g. `"You found a red potion! +5 health"`)

✅ **Submission**: Share your updated battle system with your mentor.

---

#### ✏️ **Day 4: Add a Goal & Winning Condition**

🎯 **Objective**: Add an ending for the game (winning or losing)
🧠 **Concepts**: booleans, `if/else`, creative writing
🕒 **Estimated time**: 60 minutes

🛠 **Instructions**:

1. Add a new room: `"Treasure Room"`

2. From the Hallway, if the player types `"go east"` they should reach the Treasure Room

3. In the Treasure Room:

   * Print: `"You found the magical diamond! You win!"`
   * Set `game_over = True`

4. Make sure the player *can’t* go east unless they're in the Hallway

5. Keep printing current health and room name each turn

💡 **Challenge Extension**:
Ask for a magic password before entering the treasure room — only allow them in if they type `"abracadabra"`

✅ **Submission**: Submit your win-ending version of the game.

---

#### ✏️ **Day 5: Polish & Personalize**

🎯 **Objective**: Add flair and replay-ability
🧠 **Concepts**: creativity, polish, reuse
🕒 **Estimated time**: 60–75 minutes

🛠 **Instructions**:

1. At the start of your game, print a cool ASCII title or dungeon name like:

   ```
   🏰 DUNGEON OF DECISIONS 🏰
   ```

2. Use `f-strings` for all your prints to make them colorful and fun

3. Add 2+ fun surprises:

   * Random silly messages ("You step on a jellybean!")
   * Special commands ("say hi" → "Hi, brave explorer!")

4. Print a summary when game ends:

   * How many rooms they entered
   * Their final health
   * A message based on if they won or lost

💡 **Challenge Extension**:
Wrap the entire game in a function called `play_game()` so they can replay it by typing that again!

✅ **Submission**: Final version of your dungeon game — submit the complete Python file. Bonus: include emojis!
