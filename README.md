 1. ATM prgm


package atm;
import java.util.Scanner;

public class atm123 {
	
	public static void main(String arg[]) {
		int i=0, dpin=8123,ipin;
		Scanner s=new Scanner(System.in);
		do {
			System.out.println("Please enter pin:");
			ipin=s.nextInt();
			if(ipin==dpin) {
				menu();
			}
			else {
				System.out.println("Wrong pin");
				i++;
			}
		}while(i<3);
	}
	static void menu() {
		int j=0,amt=6000;
		do {
			System.out.println("1. Deposit");
			System.out.println("2. Withdraw");
			System.out.println("3. Balance");
			System.out.println("4. Exit");
			Scanner choi=new Scanner(System.in);
			int c=choi.nextInt();
			
			switch(c) {
			case 1:
				System.out.println("Enter the amount you want to deposit:");
				Scanner d=new Scanner(System.in);
				int dep=d.nextInt();
				if(dep%500==0) {
				amt+=dep;
				System.out.println("Deposited");
				}
				else {
					System.out.println("Enter in terms of 500");
				}
				
				break;
			case 2:
				System.out.println("Enter the amount you want to withdraw:");
				Scanner w=new Scanner(System.in);
				int wd=w.nextInt();
				if(wd%500==0) {
				if(wd>amt) {
					System.out.println("Balance insufficient.");
					break;
				}
				else {
					amt=amt-wd;
				} }
				else {
					System.out.println("Enter in terms of 500");
				}
				break;
			case 3:
				System.out.println("Balance is:"+amt);
				break;
			case 4:
				System.exit(0);
			default:
				System.out.println("Please enter correct value.");
			}
		}while(true);
	}	

}



2. triangle problem


package tri;

import java.util.Scanner;

public class tri123 {
	public static void main(String[] args){
		Scanner s=new Scanner(System.in);
		int O=1;
		do{
		System.out.println("Enter 3 inputs which are the sides of a triangle");
		int a=s.nextInt();
		int b=s.nextInt();
		int c=s.nextInt();
		if(a<=200 && b<=200 && c<=200 && a>=1 && b>=1 && c>=1)
		{
		if(a<b+c && b<a+c && c<a+b){
		if(a==b && b==c)
		{
		System.out.println("It is an equilateral triangle\n");
		}
		else if(a==b||b==c||c==a)
		{
		System.out.println("It is an isoceles triangle\n");
		}
		else
		{
		System.out.println("It is a scalene triangle\n");
		}
		}
		else
		System.out.println("It is not a triangle\n");
		}
		else
		System.out.println("Invalid input\nEnter sides within the range 1-200\n");
		System.out.println("1. To enter input\n 2.to exit\nEnter your choice ");
		O=s.nextInt();
		}while(O!=2);
		s.close();
		}
		}






import org.openqa.selenium.chrome.ChromeDriver;

public class title {

public static void main(String[] args) {
// TODO Auto-generated method stub
	System.setProperty("webdriver.chrome.driver","D:\\Downloads\\chromedriver_win32\\chromedriver.exe");
ChromeDriver driver = new ChromeDriver();
driver.get("https://www.google.co.in/");
driver.manage().window().maximize();
String str=driver.getTitle();
String str1=driver.getCurrentUrl();
System.out.println("title of this web is'"+str+"'");
System.out.println("url of this web is'"+str1+"'");

if(str.equals("Google") && str1.equals("https://www.google.co.in/") ){
 System.out.println(true);}

else {

System.out.println(false);
}


}
}
