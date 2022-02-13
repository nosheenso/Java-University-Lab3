// Java-University-Lab3

public class SavingsAccount extends BankAccount {

	/* Additional instance variable on the inherited variables from BankAccount class */
	private double interestRate;
	
	/*Constructor */
	public SavingsAccount(double initialAmount, double rate) {
		super(initialAmount);
		interestRate = rate;
	}
	
	/*Getter method to get Interest Rate */
	public double getInterestRate() {
		return interestRate;
	}
	
	/*Method to calculate Interest*/
	public void calculateInterest() {
		deposit(getBalance() * interestRate);
	}
	
	/*toString Method*/
	public String toString() {
		return("SavingsAccount: balance $" + getBalance() + ", interest rate " + getInterestRate());
	}
	
	/*Main method*/
	public static void main(String[] args) {
        SavingsAccount myAccount = new SavingsAccount(100.0,0.15);
	myAccount.calculateInterest();
	System.out.println(myAccount.toString());
	
	}
	
	
}
