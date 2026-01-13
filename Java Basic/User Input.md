
---
## Scanner
- `Scanner` is an object that allows us to accept user input in ==JAVA.==
- First need to import `Scanner` at top  of the java file:
```
import java.util.Scanner;

public class  Main {
	public static void main(Sting[] args) {
	}
}
```
--> *Here `util`  is a package and `Scanner` is a class.
- Then create a `Scanner` object : `Scanner scanner = new Scanner(System.in);`
- Close the `Scanner`:  `scanner.close();`--> *if we don't close `Scanner` that can lead to unexpected behavior*
- Creating a prompt within our console: `System.out.println("Enter your name:");`
- After that need to  take input from user: `scanner.nextLine();`-->  *User will be able to type their name.*
- This user input not doing anything so  need *assign* a `Variable` with it.  

---
####  Taking input with `Variable`
- Declaring ==Variable==: 
		*String:*  `String name =  scanner.nextLine();`
		*Int:*  `int name = scanner.nextInt();`
		*double:* `double gpa = scanner.nextDouble();`
		*boolean:* `boolean isStudent =  scanner.nextBoolean();`
- If we use `scanner.next()` instead of `scanner.nextLine()`--> *that cannot read the space between string and output will be show only word which one get before space.*

**Code & Output**

```
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args ) {  
        Scanner input = new Scanner(System.in);  
  
//  Taking String Value From User  
        System.out.print("Enter Your Name:");  
        String name = input.nextLine();  
  
//  Taking Integer Value From User  
        System.out.print("Enter Your Age:");  
        int age = input.nextInt();  
  
//  Taking Double Value From User  
        System.out.print("Enter Your GPA:");  
        double gpa = input.nextDouble();  
  
//  Taking Boolean Value From User  
        System.out.print("Are you a Student? (true/false):");  
        boolean isStudent = input.nextBoolean();  
  
//  Showing the Output  
        System.out.println("Hello," + name);  
        System.out.println("Your Age is " + age);  
        System.out.println("Your GPA is " + gpa);  
  
        if(isStudent) {  
            System.out.println("You are enrolled in a Student");  
        }  
        else {  
            System.out.println("You are not enrolled in a Student");  
        }  
  
        input.close();  
    }  
}
```

*Output:*

```
Enter Your Name: Md. Eftear Islam
Enter Your Age: 26
Enter Your GPA: 3.82
Are you a Student? (true/false): true
Hello, Md. Eftear Islam
Your Age is 26
Your GPA is 3.82
You are enrolled in a Student
```


 
> [!NOTE] There is an issue
> *If we take other Variables like `int` , `double` before `String` Variable, then the compiler cannot take the `String` Variable input*
> Demonstrating the issue through *code* and *output*

```
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args ) {  
        Scanner input = new Scanner(System.in);  
  
        System.out.print("Enter Your Age: ");  
        int age = input.nextInt();  
  
        System.out.print("Enter your favourite colour is ");  
        String colour = input.nextLine();  
  
        System.out.println("You are " +  age + " years old.");  
        System.out.println("You like the colour " + colour);  
  
  
        input.close();  
    }  
}
```

```
Enter Your Age: 26
Enter your favourite colour is You are 26 years old.
You like the colour 
```


> [!NOTE] Solution of this issue (*Input buffer*)
> *After accepting other variables  at first then we need to use `input.nextLine();` to get `String` input.* 
