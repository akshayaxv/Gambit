# **Gambit: Chess Playing Website**

**Gambit** is a modern, interactive chess-playing website where users can play against a computer. It provides a clean, responsive interface along with essential chess features such as board flipping, setting custom positions, and support for FEN notation. Whether you're a beginner or an experienced player, Gambit is designed to enhance your chess experience with smooth gameplay and educational tools.

## **Features**

- **Play Against the Computer**: Engage in a game against an AI opponent of varying difficulty levels.
- **Flip the Board**: Easily switch perspectives between White and Black.
- **Set Custom Positions**: Manually set up specific board positions for practice or analysis using FEN notation.
- **FEN Notation Support**: Load and share specific chess positions using Forsyth-Edwards Notation.
- **Legal Move Validation**: Chess rules are enforced, ensuring that only legal moves can be made.
- **Castling & En Passant**: Full support for special moves like castling and en passant.

## **Technologies and Libraries Used**

**Gambit** is built using the following frontend tools and libraries:

- **HTML/CSS/JavaScript**: Core technologies for building the user interface and handling gameplay interaction.
- **chessboard.js**: A powerful JavaScript library used to render the interactive chessboard.
- **chess.js**: A comprehensive chess engine that handles game logic, move validation, and legal moves based on the current board state.


## **FEN Notation in Gambit**

### **What is FEN?**
**FEN** (Forsyth-Edwards Notation) is a widely-used standard for representing the current position of a chess game. It provides a compact and readable way to describe the layout of the chess pieces on the board, along with additional game information such as which player's turn it is, castling rights, and more. This notation is supported by Gambit for setting up and saving chess positions.

### **Structure of a FEN String**

A FEN string is divided into six fields, each separated by a space. These fields contain all the information necessary to recreate a specific chess position:

1. **Piece Placement (8 ranks)**: This field represents the position of pieces on the board, rank by rank, starting from the 8th rank (top of the board). Each rank is described using characters for the pieces and numbers for empty squares:
   - **K** for White king
   - **Q** for White queen
   - **R** for White rook
   - **B** for White bishop
   - **N** for White knight
   - **P** for White pawn
   - **k** for Black king
   - **q** for Black queen
   - **r** for Black rook
   - **b** for Black bishop
   - **n** for Black knight
   - **p** for Black pawn  
   Numbers from 1 to 8 are used to represent consecutive empty squares. For instance, `rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR` represents the starting position of a chess game, with each rank separated by a forward slash (/).

2. **Active Color**: This field indicates whose turn it is to move:
   - **w** for White's turn
   - **b** for Black's turn

3. **Castling Availability**: This field records whether castling is still possible for either side:
   - **K** for White kingside castling (with the rook on the h-file)
   - **Q** for White queenside castling (with the rook on the a-file)
   - **k** for Black kingside castling
   - **q** for Black queenside castling  
   A hyphen (-) is used if neither side can castle.

4. **En Passant Target Square**: If a pawn has moved two squares forward from its starting position, this field indicates the square where an en passant capture is possible. If no en passant capture is available, this field is marked with a hyphen (-).

5. **Halfmove Clock**: This field shows the number of half-moves (also known as "plies") since the last pawn move or piece capture. This is used to track the fifty-move rule, which can lead to a draw if no pawn move or capture occurs in fifty consecutive moves.

6. **Fullmove Number**: This field represents the number of full turns played in the game, starting at 1 and increasing after each of Black's moves.

### **Example of a FEN String**

```bash
rnbqkb1r/ppp1pppp/5n2/3p4/3P4/8/PPP2PPP/RNBQKBNR w KQkq - 0 4
```
This string describes a chess position where:
- It's White's turn to move.
- Both sides can still castle kingside and queenside.
- There is no en passant possibility.
- No pawn moves or captures have occurred in the last half-move.
- The game is currently in its 4th full move.

### **Using FEN in Gambit**

In **Gambit**, you can input a FEN string to load a specific chess position for practice or analysis. This feature allows you to recreate famous games, try out different scenarios, or set up custom board configurations for teaching or studying chess tactics.

By supporting FEN notation, **Gambit** enhances its flexibility and ensures that players have a versatile tool for exploring a wide variety of chess positions.


## **How to Run the Project**

### **Prerequisites**
To run Gambit locally, you will need:
- A modern web browser (Chrome, Firefox, Edge, etc.)
- A text editor or IDE (e.g., Visual Studio Code)

### **Steps to Run Locally**

1. **Clone the Repository**  
   Run the following command in your terminal to clone the repo:
   ```bash
   git clone https://github.com/your-username/gambit.git
   ```

2. **Open the Project**  
   Navigate to the project directory and open `index.html` in your web browser.
   ```bash
   cd gambit
   ```

3. **Start Playing**  
   The chessboard will be displayed in your browser, and you can immediately start playing by choosing to be either White or Black.



## **License**

This project is licensed under the MIT License. Feel free to use, modify, and distribute the code in any personal or commercial projects.

---

We hope **Gambit** brings you an enjoyable and educational chess experience! Happy playing!
