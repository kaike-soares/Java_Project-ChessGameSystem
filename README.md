<h1 align="center">Projeto: Sistema jogo de xadrez</h1>

![chess-system-design](https://user-images.githubusercontent.com/62703587/111727080-f7b83700-8848-11eb-8ffb-9d534284f294.png)


## First class: Position
1. Class Position [public]
2. OOP Topics:
	- Encapsulation
	- Constructors
	- ToString (Object / overriding)

## Starting to implement Board and Piece
1. Classes Piece, Board [public]
2. OOP Topics:
	- Associations
	- Encapsulation / Access Modifiers
	- ToString (Object / overriding)
3. Data Structures Topics:
	- Matrix

## Chess layer and printing the board
		8 - - - - - - - -
		7 - - - - - - - -
		6 - - - - - - - -
		5 - - - - - - - -
		4 - - - - - - - -
		3 - - - - - - - -
		2 - - - - - - - -
		1 - - - - - - - -
		  a b c d e f g h

1. Methods: Board.Piece(row, column) and Board.Piece(position)
2. Enum Chess.Color
3. Class Chess.ChessPiece [public]
4. Class Chess.ChessMatch [public]
5. Class ChessConsole.UI
6. OOP Topics:
	- Enumerations
	- Encapsulation / Access Modifiers
	- Inheritance
	- Downcasting
	- Static members
	- Layers pattern
7. Data Structures Topics:
	- Matrix
 
## Placing pieces on the board 
1. Method: Board.PlacePiece(piece, position)
2. Classes: Rook, King [public]
3. Method: ChessMatch.InitialSetup
4. OOP Topics:
	- Inheritance
	- Overriding
	- Polymorphism (ToString)

## BoardException and defensive programming 
1. Class BoardException [public]
2. Methods: Board.PositionExists, Board.ThereIsAPiece
3. Implement defensive programming in Board methods
4. OOP Topics:
	- Exceptions
	- Constructors (a string must be informed to the exception)

## ChessException and ChessPosition 
1. Class ChessException [public]
2. Class ChessPosition [public]
3. Refactor ChessMatch.InitialSetup
4. OOP Topics:
	- Exceptions
	- Encapsulation
	- Constructors (a string must be informed to the exception)
	- Overriding
	- Static members
	- Layers pattern

## Moving pieces 
1. Method Board.RemovePiece
2. Method UI.ReadChessPosition
3. Method ChessMatch.PerformChessMove
	- Method ChessMatch.MakeMove
	- Method ChessMatch.ValidadeSourcePosition
4. Write basic logic on Program.cs
5. OOP Topics:
	- Exceptions
	- Encapsulation

## Handling exceptions and clearing screen
1. Clear screen using Java:
	https://stackoverflow.com/questions/2979383/java-clear-the-console

			public static void clearScreen() {
				System.out.print("\033[H\033[2J");
				System.out.flush();
			}

	- ChessException
	- InputMismatchException

 
<h4 align="center"> 
	🚧  🚀 Em construção...  🚧
</h4>

