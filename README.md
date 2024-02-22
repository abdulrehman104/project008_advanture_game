# Fuel Fight Game

This is a simple text-based game called "Fuel Fight" where you, as the player, combat various opponents by managing your fuel levels wisely. The game is built using Node.js and utilizes libraries like inquirer for interactive prompts and chalk for colorful console output.

## Gameplay

- **Player Initialization:** At the start of the game, you'll be prompted to enter your name and choose an opponent from a list including Skeleton, Zombie, and Tiger.
- **Game Loop:** The game runs in a loop where you and your opponent take turns attacking each other or healing.
- **Fuel Management:** Both you and your opponent start with full fuel (100%). Each attack consumes 25% of your fuel. If your fuel reaches 0, you lose the game.
- **Victory Condition:** Your goal is to defeat your opponent by reducing their fuel to 0 before yours runs out.
- **Choices:** During your turn, you can choose to either attack, heal, or exit the game.

## How to play

- Clone this repository to your local machine.
- Navigate to the project directory in your terminal.
- Run npm install to install the dependencies.
- Start the game by running npm start.
- Follow the prompts to play the game.

## Technologies Used

- **Node.js:** The game is built using JavaScript and runs on the Node.js runtime.
- **inquirer:** Used for interactive command-line prompts.
- **chalk:** Utilized for colorful console output.

# **Game Implementation Overview**



**Overview of a Simple Console-Based Game Implementation**

1. **Player Class (Player.ts)**:

   - The Player class represents an object that manages the details and actions of a player.
   - **Properties**:
     - `name`: The name of the player, initialized through the constructor.
     - `fuel`: The fuel level of the player, defaulting to 100.
   - **Methods**:
     - `DecFuel()`: Method to decrease the player's fuel level by 25 units.
     - `IncFuel()`: Method to increase the player's fuel level to 100 units.
   - **Example**:
     ```typescript
     let p1 = new Player("Abdul");
     ```

2. **Opponent Class (Opponent.ts)**:

   - The Opponent class represents an object that battles against the player.
   - **Properties**:
     - `name`: The name of the opponent, initialized through the constructor.
     - `fuel`: The fuel level of the opponent, defaulting to 100.
   - **Methods**:
     - `DecFuel()`: Method to decrease the opponent's fuel level by 25 units.
   - **Example**:
     ```typescript
     let o1 = new Opponent("Skeleton");
     ```

3. **Inquirer for Player and Opponent Selection**:

   - Inquirer library is used to select the player and opponent.
   - **Example**:
     ```typescript
     let playerName = await inquirer.prompt([
       {
         type: "input",
         name: "name",
         message: "Enter your name ",
       },
     ]);
     ```

4. **Game Loop**:

   - The main loop of the game continues until the game ends.
   - **Example**:
     ```typescript
     do {
       // Game logic here
     } while (true);
     ```

5. **Player Actions**:

   - Player actions include Attack, Heal, and Exit the game.
   - Input for each action is obtained using Inquirer.
   - **Example**:
     ```typescript
     if (ask.name == "Attack") {
       // Attack logic here
     }
     ```

6. **Logic Based on Opponent Selection**:

   - Corresponding logic is implemented based on the opponent selected.
   - Each opponent has unique logic.
   - **Example**:
     ```typescript
     if (OponentName.name == "Skeleton") {
       // Specific logic for Skeleton here
     }
     ```

7. **Game End Conditions**:
   - The game ends when either the player's or the opponent's fuel level reaches 0.
   - Appropriate messages are displayed based on the end condition.
   - **Example**:
     ```typescript
     if (p1.fuel <= 0) {
       console.log(chalk.red.bold.italic("You lose better luck next time"));
       break;
     }
     ```

This code implements basic game logic allowing the player to battle against different opponents until either the player exits or the fuel level of any participant drops to 0.
