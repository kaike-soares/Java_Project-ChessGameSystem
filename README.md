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
1. Clear screen using Java:<br>
	https://stackoverflow.com/questions/2979383/java-clear-the-console

			public static void clearScreen() {
				System.out.print("\033[H\033[2J");
				System.out.flush();
			}

	- ChessException
	- InputMismatchException

## Possible moves of a piece
![1](https://user-images.githubusercontent.com/62703587/113467178-a21e8580-9417-11eb-9be3-2010b78c054b.PNG)
![2](https://user-images.githubusercontent.com/62703587/113467346-d47cb280-9418-11eb-9b5e-014c1945e28e.PNG)

1. Methods in Piece:
	- PossibleMoves [abstract]
	- PossibleMove
	- IsThereAnyPossibleMove
2. Basic PossibleMove implementation for Rook and King
3. Update ChessMatch.ValidadeSourcePosition
4. OOP Topics:
	- Abstract method / class
	- Exceptions	

## Implementing possible moves of Rook
1. Method ChessPiece.IsThereOpponentPiece(position)[protected]
2. Implement Rook.PossibleMoves
3. Method ChessMatch.ValidateTargetPosition
4. OOP Topics:
	- Polymorphism
	- Encapsulation / access modifiers [protected]
	- Exceptions

# Printing possible moves
1. Method ChessMatch.PossibleMoves
2. Method UI.PrintBoard [overload]
3. Refactor main program logic
4. OOP Topics:
	- Overloading

## Implementing possible moves of King
1. Method King.CanMove(position)[private]
2. Implement King.PossibleMoves
3. OOP Topics:
	- Encapsulation
	- Polymorphism	

## Switching player each turn
1. Class ChessMatch
	- Properties Turn, CurrentPlayer [private set]
	- Method NextTurn [private]
	- Update PerformChessMove
	- Update ValidateSourcePosition
2. Method UI.PrintMatch
3. OOP topics
	- Encapsulation
	- Exceptions

## Handling captured pieces
1. Method UI.PrintCapturedPieces
2. Update UI.PrintMatch
3. Update Program logic
4. Lists in ChessMatch:_piecesOnTheBoard, _capturedPieces
	- Update constructor
	- Update PlaceNewPiece
	- Update MakeMove
5. OOP Topics:
	- Encapsulation
	- Constructors
6. Data Structures Topics:
	- List		

## Check logic
- Rules:
	- Check means your king is under threat by at least one opponent piece
	- You can't put yourself in check

1. Property ChessPiece.ChessPosition [get]
2. Class ChessMatch:
	- Method UndoMove
	- Property Check [private set]
	- Method Opponent [private]
	- Method King(color) [private]
	- Method TestCheck
	- Update PerformChessMove
3. Update UI.PrintMatch
				
## Checkmate logic
1. Class ChessMatch
	- Property Checkmate [private set]
	- Method TestCheckmate [private]
	- Update PerformChessMove
2. Update UI.PrintMatch
	- Method UndoMove
3. Update Program logic

## Piece move count
1. Class ChessPiece:
	- Property MoveCount [private set]
	- Method IncreaseMoveCount [internal]
	- Method DecreaseMoveCount [internal]
2. Class ChessMatch:
	- Update MakeMove
	- Update UndoMove
3. OOP Topics:
	- Encapsulation
 
<h4 align="center"> 
	🚧  🚀 Em construção...  🚧
</h4>

