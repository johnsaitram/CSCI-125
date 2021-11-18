## Write a Java program that contains a method to get a number from the user and print whether it is positive or negative:

    import java.util.Scanner;

    public class MethodPrint {
	


	public static void main(String[] args) {

    /* u is for user input */
    
		int u ; 
		
		Scanner input = new Scanner(System.in);        
		System.out.print("Enter an integer: ");        
		u = input.nextInt();        
		// closing the scanner object    
		input.close();    
			
		if(u>0) {
			System.out.println("Your number is positive");
			
		} else if(u<0){
			System.out.println("Your number is negative");

		} else {
			System.out.println("Your number is 0");
		}

	}

	
    }


## Write a Java program that contains a method to take three numbers from the user and print the greatest number:
    
    import java.util.Scanner;


    public class MethodPrintGreatest {

	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int a;
		int b;
		int c;
		
		Scanner input = new Scanner(System.in);        
		System.out.print("Enter an integer: ");        
		a = input.nextInt();
		System.out.print("Enter an integer: ");
		b = input.nextInt();
		System.out.print("Enter an integer: ");
		c = input.nextInt();
		input.close();  
		
		
	if(a>b && a>c) {
		System.out.println(" User input for A is the greatest number");
	}
	if (b>a && b>c) {
		System.out.println("User input for B is the greatest number");
	}
	if (c>a && c>b) {
		System.out.println("User input for C is the greatest number");
	}
	if (a==b && b==c) {
		System.out.println("User inputed all the same numbers");
	}
    }
    }


## Write a Java program that keeps a number from the user and generates an integer between 1 and 7 and displays the name of the weekday:

    import java.util.Scanner;

    public class NumberAndDays {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		
		
		// TODO Auto-generated method stub
		int day;
		
		Scanner input = new Scanner(System.in);        
		System.out.print("Enter an integer: ");        
		day = input.nextInt();
		input.close();    

		
	String dayString="Our Burger King Work Schedule starts on Friday(1) and ends on Thursday(7)";
	
	switch(day) {
	case 1: dayString="1 - Friday";
	break;
	case 2: dayString="2 - Saturday";
	break;
	case 3: dayString="3 - Sunday";
	break;
	case 4: dayString="4 - Monday";
	break;
	case 5: dayString="5 - Tuesday";
	break;
	case 6: dayString="6 - Wednesday";
	break;
	case 7: dayString="7 - Thursday";
	break;
	default:System.out.println("That isn't a valid input! Please try again.");
	}
	System.out.println(dayString);
		
	}

    }


	

