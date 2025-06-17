# Banking_using_java
This is an Java console-based banking application simulates a simple bank account management system. It allows the user to view their balance, deposit funds, and withdraw money, with interactive menu-driven options.


#code
import java.util.Scanner;
public class Banking {
	static Scanner sc = new Scanner(System.in);
	public static void main(String[] args) {
		
		double balance=0;
		int choice;
		boolean isRunning= true; 
		
while(isRunning){
	System.out.println("---------------------");
	System.out.println("Banking in Java:");
	System.out.println("---------------------");
	System.out.println("1.Showbalance");
	System.out.println("---------------------");
	System.out.println("2.Deposit");
	System.out.println("---------------------");
	System.out.println("3.Withdraw");
	System.out.println("---------------------");
	System.out.println("4.Exit");
	System.out.println("---------------------");
	System.out.println("Enter a choice of 1-4:");
	choice = sc.nextInt();
	switch(choice){
	case 1 -> ShowBalance(balance);
	case 2 -> balance+=Deposit();
	case 3 -> balance-=Withdraw(balance);
	case 4 -> isRunning = false;
	default -> System.out.println("D");
	}
}
System.out.println("---------------------");
System.out.println("Thanks!forUsing");
System.out.println("---------------------");
}
		static void ShowBalance(double balance) {
			System.out.println("---------------------");
			System.out.printf("$%.2f\n", balance);
}
		static double Deposit() {
			double amount;
			amount = sc.nextDouble();
			return amount;
		}
		static double Withdraw(double balance){
			double amount;
			amount = sc.nextDouble();
			if(amount>balance)
			{
				System.out.println("NO AMOUNT");
			}else {
				return 0;
			}
			return 0;
		}
}

