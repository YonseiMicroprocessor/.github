# 8x8 Card Game Project

This project is an Arduino-based card game implemented as part of the **Microprocessor** course at Yonsei University. The game takes place on an 8x8 grid, where 42 cards are revealed in each turn, and characters move based on the card's suit. The goal is for a character to reach the target row first.

# Logo
![Logo](https://github.com/user-attachments/assets/13f52d47-91a0-4575-ba3e-fff558ff6f70)


## Game Rules

1. **Game Start**  
   - The game board consists of an 8x8 grid. The game starts with the four suit A cards (Spade, Diamond, Heart, and Clover) placed in the bottom row, one by one with a space in between.
   - Bonus cards are placed randomly in 6 out of the 8 spaces in the rightmost column (excluding the first and last cells). The bonus cards are selected randomly from the 48 remaining cards (from 2 to King).

2. **Game Progression**  
   - The game is played over 42 turns.
   - In each turn, one card is drawn and flipped. The character corresponding to the suit of the drawn card moves forward by one space.
   - When all characters pass the row with the bonus cards (starting from the second row from the bottom), the bonus cards are revealed. The characters corresponding to the suit of the bonus card will move backward by one space.

3. **Game End Condition**  
   - The game ends if any character reaches the top row during the 42 turns.
   - If no character reaches the top row, the character at the highest row at the end of 42 turns wins.

4. **Special Features**  
   - When the game ends, all LEDs light up, and the LCD displays the winning suit.
   - Each suit corresponds to a different color of light: Spade and Clover characters are highlighted in green, while Heart and Diamond characters are highlighted in red.

## Technologies Used

- **Hardware**: Arduino, 8x8 LED Matrix, 7-Segment Display, LCD
- **Software**: Arduino IDE

## Installation Instructions

1. Install the Arduino IDE and upload the provided code to your Arduino board.
2. Connect the 8x8 LED matrix, 7-segment display, and LCD to your Arduino.
3. Run the project, and the game will start automatically.

## Code Explanation

- **Card Deck Initialization**: The suits of the cards and the placement of the bonus cards are initialized.
- **Game Progression**: 42 cards are drawn sequentially, and characters move forward or backward based on the card's suit.
- **Bonus Card Handling**: When a character passes the bonus card row, the corresponding suit's character moves backward.
- **LCD Display**: The LCD displays the suit of the card drawn, bonus cards, and the number of remaining cards.
- **LED Display**: The LED color changes based on the character's suit, indicating its movement and state.

## Contributing

This project is for academic purposes. If you'd like to contribute, please fork this repository and submit a pull request.

## License

MIT License.
