# Tic-Tac-Toe with SwiftUI

Welcome to the **Tic-Tac-Toe** game built using **Swift** and **SwiftUI**! This project demonstrates how to create a simple yet engaging Tic-Tac-Toe game using SwiftUI's powerful layout tools like `HStack`, `VStack`, and `ZStack`. Whether you're a beginner or an experienced Swift developer, this project will help you understand how to structure a game UI and manage state in SwiftUI.

## Features

- **Interactive Gameplay**: Play a classic 3x3 Tic-Tac-Toe game against a friend.
- **Dynamic UI**: Built using SwiftUI's `HStack`, `VStack`, and `ZStack` for a clean and responsive layout.
- **Win Detection**: Automatically detects when a player wins or if the game ends in a draw.
- **Reset Game**: Easily reset the game to start a new round.

## Screenshots

![Screenshot 1](screenshots/screenshot1.png)  
*The game board with X and O moves.*

![Screenshot 2](screenshots/screenshot2.png)  
*Win detection and game reset option.*

## How It Works

The game leverages SwiftUI's declarative syntax to create a dynamic and interactive UI. Here's a breakdown of the key components:

1. **Game Board**: The 3x3 grid is created using nested `HStack` and `VStack` views.
2. **Player Moves**: Each cell in the grid is a `Button` that updates the game state when tapped.
3. **Win Detection**: The game checks for winning combinations after each move using a simple algorithm.
4. **Reset Functionality**: A "Reset" button clears the board and resets the game state.

### Code Example

Here's a snippet of how the game board is structured using `HStack` and `VStack`:

```swift
VStack {
    ForEach(0..<3) { row in
        HStack {
            ForEach(0..<3) { column in
                Button(action: {
                    // Handle player move
                }) {
                    Text(self.gameBoard[row][column])
                        .font(.largeTitle)
                        .frame(width: 80, height: 80)
                        .background(Color.blue.opacity(0.2))
                        .cornerRadius(10)
                }
            }
        }
    }
}
```

The `ZStack` is used to overlay the game board with a win message or reset button when the game ends.

## Requirements

- Xcode 12 or later
- iOS 14 or later
- Swift 5.3 or later

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/tictactoe-swiftui.git
   ```
2. Open the project in Xcode.
3. Build and run the project on the iOS Simulator or a physical device.

## Contributing

Contributions are welcome! If you have any ideas, improvements, or bug fixes, feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Enjoy playing Tic-Tac-Toe! If you have any questions or feedback, feel free to reach out. Happy coding! 🚀
