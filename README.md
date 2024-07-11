# Welcome to "Acerte o Número" | by: @CAUEENRICO.DEV em uma madrugada explorando o C#

## Game Description

"Acerte o Número" is a simple and fun console game developed in C#. The objective of the game is to guess the correct number between 1 and 10. If you guess the lucky number, you will win a million pix in your account!

## Game Features

- **Random Number Generation:** The game generates a random number between 1 and 10.
- **User Input:** Players can input their guess through the console.
- **Hints:** If the guess is incorrect, the game provides hints whether the number is higher or lower than the guess.
- **Winning Message:** When the correct number is guessed, a congratulatory message is displayed.

## How to Play

1. **Run the Game:** Start the game by running the C# code in a console environment.
2. **Guess the Number:** You will be prompted to guess a number between 1 and 10.
3. **Receive Feedback:** If your guess is incorrect, you will receive a hint telling you if the correct number is higher or lower than your guess.
4. **Win the Game:** Keep guessing until you find the correct number. When you guess correctly, you will receive a winning message.

## Code

```csharp
// Acerte o Número

Console.WriteLine(@"
░██████╗░██╗░░░██╗███████╗░██████╗░██████╗  ███╗░░░███╗██╗██╗░░░░░██╗░░░░░██╗░█████╗░███╗░░██╗
██╔════╝░██║░░░██║██╔════╝██╔════╝██╔════╝  ████╗░████║██║██║░░░░░██║░░░░░██║██╔══██╗████╗░██║
██║░░██╗░██║░░░██║█████╗░░╚█████╗░╚█████╗░  ██╔████╔██║██║██║░░░░░██║░░░░░██║██║░░██║██╔██╗██║
██║░░╚██╗██║░░░██║██╔══╝░░░╚═══██╗░╚═══██╗  ██║╚██╔╝██║██║██║░░░░░██║░░░░░██║██║░░██║██║╚████║
╚██████╔╝╚██████╔╝███████╗██████╔╝██████╔╝  ██║░╚═╝░██║██║███████╗███████╗██║╚█████╔╝██║░╚███║
░╚═════╝░░╚═════╝░╚══════╝╚═════╝░╚═════╝░  ╚═╝░░░░░╚═╝╚═╝╚══════╝╚══════╝╚═╝░╚════╝░╚═╝░░╚══╝

███╗░░██╗██╗░░░██╗███╗░░░███╗██████╗░███████╗██████╗░
████╗░██║██║░░░██║████╗░████║██╔══██╗██╔════╝██╔══██╗
██╔██╗██║██║░░░██║██╔████╔██║██████╦╝█████╗░░██████╔╝
██║╚████║██║░░░██║██║╚██╔╝██║██╔══██╗██╔══╝░░██╔══██╗
██║░╚███║╚██████╔╝██║░╚═╝░██║██████╦╝███████╗██║░░██║
╚═╝░░╚══╝░╚═════╝░╚═╝░░░░░╚═╝╚═════╝░╚══════╝╚═╝░░╚═╝");

Console.WriteLine("Welcome to the Guess the Number game!");
Console.WriteLine("\n***If you guess the lucky number, you will receive a million pix in your account***");

Random random = new Random();
int SortNum = random.Next(1, 10);

do {
    Console.Write("\nGuess a number: ");
    string PutChoice = Console.ReadLine()!;
    int PutChoiceNumber = int.Parse(PutChoice);

    if (PutChoiceNumber == SortNum) {
        Console.WriteLine(@"
█▀▀ █▀█ █▄░█ █▀▀ █▀█ ▄▀█ █▀▄ █░█ █░░ ▄▀█ ▀█▀ █ █▀█ █▄░█ █▀ ░   █▄█ █▀█ █░█   █░█░█ █ █▄░█   █
█▄▄ █▄█ █░▀█ █▄█ █▀▄ █▀█ █▄▀ █▄█ █▄▄ █▀█ ░█░ █ █▄█ █░▀█ ▄█ █   ░█░ █▄█ █▄█   ▀▄▀▄▀ █ █░▀█   ▄");
        break;
    } else if (PutChoiceNumber > SortNum) {
        Console.WriteLine("Not yet, the number is less");
    } else {
        Console.WriteLine("Not yet, the number is higher");
    }
} while (true);
```

Enjoy the game and good luck!
