# task 1 

package Task;

import java.util.Scanner;

public class Task1 {

	public static void main(String[] args) {
		// Generate a random number between 1 and 100
        int randomNumber = (int) (Math.random() * 100) + 1;

        // Create a Scanner object to read user input
        Scanner scanner = new Scanner(System.in);

        // Start the game loop
        boolean guessedCorrectly = false;
        int numberOfAttempts = 0;
        System.out.println("Guess a number between 1 and 100: ");


        while (!guessedCorrectly && numberOfAttempts < 3) 
        {
           
            int userGuess = scanner.nextInt();

            if (userGuess == randomNumber) 
            {
                guessedCorrectly = true;
            } 
            else 
            {
                numberOfAttempts++;
                if (userGuess > randomNumber) 
                {
                    System.out.println("Your guess is too high.");
                } else 
                {
                    System.out.println("Your guess is too low.");
                }
            }
        }

        
        scanner.close();

        
        if (guessedCorrectly) 
        {
            System.out.println("Congratulations! You guessed correctly! The number was " + randomNumber);
        } else 
        {
            System.out.println("Sorry, you ran out of guesses. The correct answer was " + randomNumber);
        }



	}

}
