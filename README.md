import java.awt.print.PrinterException;
import java.awt.print.PrinterJob;
import java.util.Random;
import java.util.Scanner;


public class Coffee {
	
	public static void main(String[] args){
		
		Scanner input = new Scanner(System.in);
		
		System.out.println("Enter customer order \n 1. Latte \n 2. Mocha \n 3. Black");
		
		int order = input.nextInt();
		
		PrinterJob job= PrinterJob.getPrinterJob();
		
		switch (order){
		
		case 1:
			System.out.println("You have chosen the Latte coffee. Would you like it small,medium or large? Enter either 1,2 or 3\n");
			break;
		case 2:
			System.out.println("You have chosen the Mocha coffee. Would you like it small,medium or large? Enter either 1,2 or 3\n");
			break;
		case 3:
			System.out.println("You have chosen the Black coffee. Would you like it small,medium or large? Enter either 1,2 or 3\n");
			break;
		default:
			System.out.println("You have chosen an invalid option please try again\n");
			break;
		}
		int size = input.nextInt(); 
		switch (size){
		
		case 1: 
			System.out.println("You have chosen small. Would you like milk? \n press 1 for yes or 2 for no\n");
		break;
		case 2: 
			System.out.println("You have chosen medium. Would you like milk? \n press 1 for yes or 2 for no\n");
		break;
		case 3:
		System.out.println("You have chosen large. Would you like milk? \n press 1 for yes or 2 for no\n");
		break;
		default:
			System.out.println("Sorry we do not have that option available, please choose from what we have\n");
		}
		int milk= input.nextInt();
		if(milk == 1){
			System.out.println("You have chosen your coffee with milk. \n That would be £5.64 \n");
		}
		else if(milk==2){
			System.out.println("You have chosen your coffee with no milk. \n That would be £5.64\n ");
			
		}
		else
			System.out.println("Sorry I do not understand your order, could you rephrase please\n");
		
		
		
		System.out.println("Do you want your receipt printed? \n 1 for yes and 2 for no");
		
		int print = input.nextInt();
		
		if(print==1){
			
			job.printDialog();
		}
		else if (print==2){
			
			System.out.println("Thank you.");
			
		}
		else
			System.out.println("Please choose a valid response. Thank you.");
		input.close();
		}
}
		
		
