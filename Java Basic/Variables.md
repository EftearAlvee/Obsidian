- Variable is a representation of  a number, in programming variable is a reusable container for a value.
- A variable behaves as if it was the value it contains.
#### Two categories of Variables
1. *Primitive:* Simple value like number that stored directly in memory(stack)[^1]
2.  *Reference:* Actually hold memory address on the stack, they point to a location in a different area known as the heap.

[^1]: Usually In a location know as the stack

| Primitive | Reference |
| --------- | --------- |
| int       | string    |
| double    | array     |
| char      | object    |
| boolean   |           |

---
#### Two step to creating a variable
1. Declaration(`int age;`)
2. Assignment(`int age = 30`)

==*Printing value of variables:* `System.out.println("The Year is " + year);`==

==**Examples of Variables:**==
- ==int:== `int year = 2025;`--> *`int` for Integers they contains whole number.*
- ==double:== `double cgpa = 3.82;`--> *`double` are numbers that can contain decimal numbers.*
- ==char:== `char grade = 'A';`--> *`char` means characters are single characters.* 
- ==boolean:== `boolean isStudent = true;` (*boolean returns true or false*) ---> it normally using in `if`  statement like this ``
  ```
  if (isStudent)  {
	  System.out.pinttln("You are a student")
  }
  else{
  System.out.println("You are not a student")
  }
  ```
	

| **Primitive Type** | **Size**  | **Minimum**  | **Maximum**          | **Wrapper Type** |
| ------------------ | --------- | ------------ | -------------------- | ---------------- |
| `boolean`          | *-*       | *-*          | *-*                  | ==Boolean==      |
| `char`             | *16 bits* | *Unicode 0*  | *Unicode $2^{16}-1$* | ==Character==    |
| `byte`             | *8 bits*  | $-128$       | $+127$               | ==Byte==         |
| `short`            | *16 bits* | $-2^{15}$    | $+2^{15}-1$          | ==Short==        |
| `int`              | *32 bits* | $-2^{31}$    | $+2^{31}-1$          | ==Integer==      |
| `long`             | *64 bits* | $-2^{63}$    | $+2^{63}-1$          | ==Long==         |
| `float`            | *32 bits* | $IEEE_{754}$ | $IEEE_{754}$         | ==Float==        |
| `double`           | *64 bits* | $IEEE_{754}$ | $IEEE_{754}$         | ==Double==       |
| `void`             | *-*       | *-*          | *-*                  | ==Void==         |

- ==String:== `String name = "Eftear Islam"`--> ==Strings are series of characters, they have a reference data type.==
			--> *String Concatenation:* `System.out.println("Hello" + name)`
			-->*Output:* `Hello Eftear Islam`
