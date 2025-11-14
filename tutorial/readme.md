
# WIX1002 Fundamentals of Programming
## Tutorial 4: Flow of Control (Repetition)


### 1. Write statements for each of the following

* a. Find the largest integer n so that $n^{3}$ is less than 2000.
* 		int n = 0;
* 		while ((n+1) * (n+1) * (n+1) < 2000){
* 			i++;
* 		}
* 		System.out.println("The largest interger n is " + n);
* b. Display the square number of the first twelve integers starting from 1.
* 		int n = 1;
* 		while (n < 13){
* 			int m = n * n;
* 			System.out.println("The square number of " + n + " is " + m);
* 			n++;
* 		}
* c. Display a 4-by-5 matrix using random number within 0 to 100.
* 		for(int row = 1; row <= 4; row++){
* 			for(int col = 1; col <= 5; col++){
* 				int randomNum = (int)(Math.random() * 101);
* 				System.out.print(randomNum + "\t");
* 			}
* 			System.out.println();
* 		}
* 		
* d. Compute the sum of numbers from 1 to a given number.
*	import java.util.Scaneer;

*	public class SumCalculator{
*		public static void main(String[] args){
*			Scanner scanner = new Scanner(System.in);
* 			System.out.print("Given a number: ");
* 			int num = scanner.nextInt();

* 			int sum = 0;
* 			for (i = 0; i <= num; i++){
* 				sum += i;
* 			}
* 			System.out.println("The sum from 1 to " + num " is " + sum);
* 			scanner.close():
* 		}
* 	}
* 		
* e. Compute the sum of the series: 1/25+2/24+3/23 + ... + 25/1 in two decimal places.
*		double sum = 0;
* 		for（int i=1;i<=25;i++){
* 			int denominator = 26 - i;
* 			sum += (double)i / denominator;
* 		}
* 		System.out.println("The sum of the series is " + sum);

---

### 2. Correct the error for the following statements.



a. 
```java
for (x=10;x > 0;x--)
	sum += x;
```
b.
```java
int x = 0, y = 0;
do {
	x += 2;
	y += x; 
	System.out.println(x + " and " + y); 
}while (x<100);
```
c.
```java
for ( x=1, y=20; x < y; x++, y-=2){
}
	System.out.println(x + " " + y);
```
d.
```java
int i=1;
while(i<=10) {
	if (i==10){
		System.out.println("Program End");}
	i++;
}
```
---
### 3. Write the statements that display the first ten values of the Fibonacci sequence.  

Given the formula $f_{1}=1$, $f_{2}=1$, $f_{n}=f_{n-1}+f_{n-2}$
	int f1 = 1, f2 = 1;
	System.out.print(f1 + " " + f2 + " ");
	for (int i = 3; i <= 10; i++) {
    	int current = f1 + f2;
    	System.out.print(current + " ");
    	f1 = f2;
    	f2 = current;
}
---
### 4. Write the statements that display the string in reverse order.

(use `String.length()` to get the length of the string)
	String str = "WIX1002";
	String reverseStr = "";
	for (int i = str.length() - 1; i >= 0; i--) {
    	reverseStr += str.charAt(i);
	}
	System.out.println("The string in reverse order：" + reverseStr);
