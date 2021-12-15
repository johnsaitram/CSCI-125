## Backstory:

I'm thinking of a number, whoever guess it's first gets...gets what? A cookie? Gets sit in the front of the car? Time and time again we see people use this way of guessing a number from a set range to determine something, typically a prize that usaually comes with a rush of adreline. What if we can simulate that same concept of guessing a number, while delevring the satisifaction and adreline rush? Well that's what I set out to do!

## The logic!

I first started out with a very simple program. When you would start the program, it would generate a random number and store it as an integer called "random number". I then used a scanner to read user inputs and then have the scanner input then compare if that number was higer or lower to the random. Based on an if-else if-else system, it would print out a diffrent response depending on the number entered.

### Start:

![image](https://user-images.githubusercontent.com/91101494/146275229-e72ca58b-40e3-4d35-9152-1ec0e82a8e99.png)

#### If number guessed is higer than random number:

![image](https://user-images.githubusercontent.com/91101494/146275376-0281703a-9e40-4d49-b05e-59a9bb6f3ee3.png)

#### If number guessed is lower than random number:

![image](https://user-images.githubusercontent.com/91101494/146275741-91ef2a35-6217-4b14-a5c1-fb3b9167270b.png)

#### If you guessed the right number:

![image](https://user-images.githubusercontent.com/91101494/146275976-fd25a8aa-c815-4884-bc60-6e05d28b7522.png)

#### Code for the "logic":


    import java.util.Random;
    import java.util.Scanner;


    public class finaltest {

      public static void main(String[] args) {

        Random rand = new Random();
          Scanner scanner = new Scanner(System.in);

          int randomNumber = rand.nextInt(100) + 1;
          System.out.println("Random number is " + randomNumber);

          int tryCount = 0;
          while(true) {
            System.out.println("Enter your guess (1-100):");

            int playerGuess = scanner.nextInt();
            tryCount++;

            if (playerGuess == randomNumber) {
              System.out.println("Correct! You Win!");
              System.out.println("It took you " + tryCount + " tries");
              break;
            }
            else if(randomNumber > playerGuess) {
              System.out.println("Nope! The number is higher. Guess again.");
            }
            else {
              System.out.println("Nope! The number is lower. Guess again.");
            }
          }



          scanner.close();

        }
    }

	

Now when it's all done, it's great! The program does everything I inteded it to do..but it's missing something...a little something special. That's where Java Swing came in!

## Java Swing:

I needed to spice this project up! Really though, it was just bland with the scanner alone, and I defiently wouldn't get a high grade with this alone...So how can I make this project special? Well that's when I decided to do Java Swing. I already had the main logic down, now it was just to quickly and easily add some buttons and text feilds and thats it..righ? Well, it turned out being a little harder than it sounded. 

I started with taking bits and parts from Lecture 8 and building from there. 

### Startup:

![image](https://user-images.githubusercontent.com/91101494/146278824-d1e7d2f6-1daf-4c74-ab1d-27ad56ffa018.png)



### Tool tips:

    txtEnterNum.setToolTipText("Insert your number here.");
    
   ![image](https://user-images.githubusercontent.com/91101494/146279624-25c2997e-d740-4d7a-bbda-b09ebac06b87.png)

    btnGuess.setToolTipText("Click here to guess your entered number.");
    
   ![image](https://user-images.githubusercontent.com/91101494/146279717-fe7d7243-4bf8-4135-b502-2333e62aa412.png)
   
### Labels and background for too high, too low, and if you win:

    labelWin.setVisible(false);
    labelLow.setVisible(true);
		labelHigh.setVisible(false);
    ...
    getContentPane().setBackground(Color.red);
   
   ![image](https://user-images.githubusercontent.com/91101494/146281725-d1870f9d-4a1c-4f2d-b974-3e76c96c596e.png)

    
    labelWin.setVisible(false);
    labelLow.setVisible(false);
		labelHigh.setVisible(true);
    ...
    getContentPane().setBackground(Color.blue);
    
   ![image](https://user-images.githubusercontent.com/91101494/146281641-07924911-5410-489a-9b73-021f899b8fef.png)

    
    labelWin.setVisible(true);
    labelLow.setVisible(false);
		labelHigh.setVisible(false);
    ...
    getContentPane().setBackground(Color.green);
 
   ![image](https://user-images.githubusercontent.com/91101494/146281594-12fd7191-2cff-4d54-986b-841fd3206029.png)

 
 ## Conclusion:
 
 This was a really fun final project. I first was had set the logic and then took on the task of doing all the Java swing stuff. If you have any questions regarding the project or anything else, feel free to message me!
    
 
			
     
      
