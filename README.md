import java.util.Random;
import java.util.Scanner;

public class GuessingGame

{
 public static void main(String[] args) 
 {
    System.out.println("...........! WELCOME TO WORD GUESSING GAME !......." + "\n");
    Random num=new Random();
    Scanner sc =new Scanner(System.in);
    
    int randomNum = num.nextInt(100) + 1;
     System.out.println("random no is " + randomNum);
    
    while (true) 
      
    {

    System.out.println("ENTER THE NUMBER BETWEEN 1-100");

    int playerGuess= sc.nextInt();
    if(playerGuess == randomNum)
    {
      System.out.println("CONGRATS..... YOU GOT IT BUDDY");
     break;

    }
    else if(randomNum>playerGuess)
    {
      System.out.println("NO.. YOUR GUESS IS LOWER...TRY AGAIN");
    }
    else if(randomNum<playerGuess)
    {
      System.out.println("NOOO.... YOUR GUESS IS HIGHER...GUESS AGAIN");
    }
    
   }
   sc.close(); 
 }
    
}
