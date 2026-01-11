# Java_CCEE

# Main Features (har ek MCQ mein aa sakta hai):
1. Platform Independent
Java bytecode kisi bhi platform pe run ho sakta hai jahan JVM available ho
Source code → Bytecode (.class) → JVM → Machine code

2. Object-Oriented
Everything is an object (except primitives)

3. Simple
C++ se simple syntax
No pointers, no operator overloading (except + for strings)
Automatic memory management (Garbage Collection)
❓ Java me operator overloading supported hai?
✅ No, except + operator for String concatenation

❓ Why only String?
👉 Readability + simplicity
👉 Complex code avoid karne ke liye

# MCQ
Q: Which feature allows Java to run on any platform?
a) Robust  b) Portable  c) Dynamic  d) Secure
Answer: b) Portable

Q: Java does NOT support?
a) Multiple inheritance through classes  b) Interfaces  c) Polymorphism  d) Encapsulation
Answer: a) Multiple inheritance through classes

Q: Which handles automatic memory management in Java?
a) JVM  b) Garbage Collector  c) JIT Compiler  d) ClassLoader
Answer: b) Garbage Collector

Q: Java is called platform independent because?
a) It uses JVM  b) It generates bytecode  c) Both a and b  d) None
Answer: c) Both a and b
Q: Which component loads .class files?
a) JIT  b) ClassLoader  c) Garbage Collector  d) Interpreter
Answer: b) ClassLoader

# JVM Kya Hai?
Java Virtual Machine - Ye ek virtual machine hai jo Java bytecode ko execute karta hai. Ye platform-specific hai.

Q: Where are objects stored in JVM?
a) Stack  b) Heap  c) Method Area  d) PC Register
Answer: b) Heap

Q: Which is shared among all threads?
a) Stack  b) PC Register  c) Heap  d) Native Stack
Answer: c) Heap

Q: JIT compiler stands for?
a) Java Intermediate Tool  b) Just-In-Time  c) Java Internet Technology  d) None
Answer: b) Just-In-Time

Q: Which ClassLoader loads core Java classes?
a) Application  b) Extension  c) Bootstrap  d) System
Answer: c) Bootstrap

Q: Local variables are stored in?
a) Heap  b) Method Area  c) Stack  d) PC Register
Answer: c) Stack

# JDK (Java Development Kit)
JDK = JRE + Development Tools
┌────────────────────────────────┐
│            JDK                 │
│  ┌──────────────────────────┐ │
│  │         JRE              │ │
│  │  ┌────────────────────┐ │ │
│  │  │       JVM          │ │ │
│  │  │                    │ │ │
│  │  └────────────────────┘ │ │
│  │  + Libraries           │ │
│  └──────────────────────────┘ │
│  + Development Tools           │
│    (javac, javadoc, jar, etc.) │
└────────────────────────────────┘
Complete development environment
Contains: JRE + Development tools
Use: Java programs develop karne ke liye

Development Tools:

javac - Compiler (.java → .class)
java - Interpreter/Launcher
javadoc - Documentation generator
jar - Archive tool
javap - Disassembler
jdb - Debugger

# JRE (Java Runtime Environment)

Runtime environment
Contains: JVM + Libraries
Use: Java programs run karne ke liye (development nahi)

Q: JRE contains?
a) JVM only  b) JVM + Libraries  c) JVM + Compiler  d) Only Libraries
Answer: b) JVM + Libraries

Q: Which is platform-dependent?
a) Java source code  b) Bytecode  c) JVM  d) JRE
Answer: c) JVM

Q: To run Java program, we need?
a) JDK  b) JRE  c) JVM  d) All of above
Answer: b) JRE (minimum requirement)

Q: javap tool is used for?
a) Compilation  b) Execution  c) Disassembling  d) Documentation
Answer: c) Disassembling

public static void main(String[] args)
```
- **public**: Accessible from anywhere
- **static**: Can be called without object
- **void**: Returns nothing
- **String[] args**: Command-line arguments

**Valid variations:**
- `public static void main(String args[])`
- `static public void main(String[] args)`
- `public static void main(String... args)` (varargs)

**6. Variables Types:**
- **Local**: Method ke andar
- **Instance**: Class ke andar, method ke bahar (object-specific)
- **Static**: Class ke andar, `static` keyword ke saath (class-level)

**7. Method Types:**
- **Instance method**: Object se call hota hai
- **Static method**: Class se directly call hota hai

### Execution Flow:
```
1. JVM loads class
2. Static variables initialize
3. Static blocks execute
4. main() method calls
5. Objects create (constructor calls)
```

### MCQ Focus:
```
Q: Java source file extension?
a) .jav  b) .java  c) .class  d) .jar
Answer: b) .java

Q: How many public classes can a file have?
a) 0  b) 1  c) 2  d) Unlimited
Answer: b) 1

Q: Which comes first in Java file?
a) import  b) package  c) class  d) method
Answer: b) package

Q: Main method signature is?
a) public void main(String[] args)
b) static void main(String[] args)
c) public static void main(String[] args)
d) void main(String[] args)
Answer: c) public static void main(String[] args)

Q: Which is valid main method?
a) public static void main(String args[])
b) public static void main(String... args)
c) static public void main(String[] args)
d) All of above
Answer: d) All of above

Q: File name must match with?
a) Any class name  b) Public class name  c) First class  d) Last class
Answer: b) Public class name

Q: Can we have multiple non-public classes in one file?
a) Yes  b) No  c) Only 2  d) Depends
Answer: a) Yes

### Type Conversion:

 1. Widening (Implicit/Automatic):
```
byte → short → int → long → float → double
       char  → int
javaint i = 100;
long l = i;      // Automatic conversion
float f = l;
```
2. Narrowing (Explicit/Type Casting):

```
 double d = 100.5;
int i = (int) d;      // i = 100 (decimal part lost)
int x = 130;
byte b = (byte) x;    // Data loss (out of range)
```
double d = 100.5;
int i = (int) d;      // i = 100 (decimal part lost)

int x = 130;
byte b = (byte) x;    // Data loss (out of range)
```

### Important Points for MCQ:

1. **char** is unsigned (0 to 65,535)
2. **Default values** apply only to instance variables, not local variables
3. **float** needs 'f', **long** needs 'L'
4. **boolean** only accepts true/false (not 0/1)
5. String is **NOT** a primitive type (it's a class)
6. **Wrapper classes**: Byte, Short, Integer, Long, Float, Double, Character, Boolean

### MCQ Practice:
```
Q: Size of int in Java?
a) 2 bytes  b) 4 bytes  c) 8 bytes  d) Platform-dependent
Answer: b) 4 bytes

Q: Range of byte?
a) -128 to 127  b) 0 to 255  c) -256 to 255  d) 0 to 127
Answer: a) -128 to 127

Q: Default value of boolean?
a) true  b) false  c) 0  d) null
Answer: b) false

Q: Which is valid?
a) float f = 3.14;  b) float f = 3.14f;  c) float f = 3.14F;  d) Both b and c
Answer: d) Both b and c

Q: Which is NOT a primitive type?
a) int  b) String  c) char  d) boolean
Answer: b) String

Q: Size of char in Java?
a) 1 byte  b) 2 bytes  c) 4 bytes  d) Depends
Answer: b) 2 bytes

Q: Which is correct?
a) char c = "A";  b) char c = 'A';  c) char c = 'AB';  d) char c = A;
Answer: b) char c = 'A';

Q: Default type of decimal number?
a) float  b) double  c) long  d) int
Answer: b) double

Q: Can boolean store 0 or 1?
a) Yes  b) No  c) Only 0  d) Only 1
Answer: b) No

Q: Which needs explicit casting?
a) int to long  b) double to int  c) byte to int  d) char to int
Answer: b) double to int

# Must Remember for C-CCEE:

1. Java = Platform Independent, JVM = Platform Dependent
2. JDK > JRE > JVM (containment hierarchy)
3. Heap = Objects, Stack = Local variables
4. Bootstrap > Extension > Application (ClassLoader hierarchy)
5. Package → Import → Class → Variables → Methods
6. Only one public class per file
7. File name = Public class name
8. primitive types (byte, short, int, long, float, double, char, boolean)
9. Main method: public static void main(String[] args)
10. Default integer = int, Default floating = double
11. String primitive nahi hai
12. JVM platform-dependent hai

Q6: Java is?
Tumhara: b (Purely interpreted)
Correct: c (Both compiled and interpreted)
Why: Java pehle compile hota hai (.java → .class bytecode), phir JVM interpret/JIT compile karta hai

Q12: Java supports multiple inheritance through?
Tumhara: d (Java doesn't support)
Correct: b (Interfaces)
Why: Class se multiple inheritance nahi, but Interfaces se possible hai

class A implements B, C, D { } // Valid - multiple interfaces
  class A extends B, C { }        // Invalid - multiple classes
```

### **Q20:** Dynamic loading of classes means?
- **Tumhara:** a (Compile time)
- **Correct:** b (Runtime when needed)
- **Why:** Classes **runtime pe on-demand load** hoti hain, not compile time pe

### **Q23:** Which memory area is shared among all threads?
- **Tumhara:** d (Native Method Stack)
- **Correct:** c (Heap)
- **Why:** **Heap and Method Area** shared hain. Native Method Stack **thread-specific** hai

### **Q26:** Static variables are stored in?
- **Tumhara:** a (Heap)
- **Correct:** c (Method Area)
- **Why:** 
  - **Heap** → Objects + instance variables
  - **Method Area** → Static variables + class-level data
  - **Stack** → Local variables

---

## 🎯 Key Points to Remember:

### 1️⃣ **Java Compilation Process:**
```
.java file → javac (compiler) → .class (bytecode) → JVM (interpreter/JIT) → Machine code

5️⃣ Memory Storage:

class Example {
    static int x = 10;      // Method Area
    int y = 20;             // Heap (with object)
    
    void method() {
        int z = 30;         // Stack
    }
}


🎯 What You MUST Revise:
Priority 1 (Urgent):

Variable storage locations

Static → Method Area (1 copy)
Instance → Heap (per object)
Local → Stack (per method call, NO default)


Multiple Inheritance

Class extends 1 class only
Class implements unlimited interfaces
Interface extends unlimited interfaces


JVM Memory

Shared: Heap + Method Area
Per Thread: Stack + PC Register
Stack stores: Local vars + method calls + return address



Priority 2:

Bytecode is platform-independent
Java slower due to interpretation + GC
String pool in Heap (Java 7+, earlier in Method Area)

## Java Tokens
Smallest individual unit in a Java program..
types :-..
1. Reserved Keywords(52)
2. Identifiers
```
// ✅ Valid
int age;
int _value;
int $price;
int age123;
int myVariable;

// ❌ Invalid
int 123age;      // starts with digit
int my-variable; // hyphen not allowed
int class;       // keyword
int my variable; // space not allowed
```
3. Literals (Constant Value)
4. Operarors
5. Punctuators 

##  Declaring Variables & Methods
 *. Variable Declaration
  1. Local Variables:
     // Must be initialized before use..
    // No default value..
    // Scope: within method only..
 2. Instance Variables
    class Student {
    String name;             // Instance variable
    int age = 20;
    // Has default value
    // Scope: within object
    // Created when object is created
}
3. Static Variable
   class Counter {
    static int count = 0;    // Static/Class variable
    // Has default value
    // Scope: entire class
    // Created when class is loaded
    // Shared by all objects
}

* byte, short, int, long ------------0
* float, double-------------------0.0
* char---------------'\u0000'
* Reference types --------------null
* Note: Local variables have NO default values
   
* Method Overloading
  ```

**Rules for Overloading:**
- Same method name
- Different parameter list (number or type)
- Return type doesn't matter for overloading
- Must be in same class or parent-child

Q: Static variable created when?
a) Object creation  b) Class loading  c) Method call  d) JVM starts


## 🎯 Key Points to Remember:
```
byte a = 10;
byte b = 20;
byte c = a + b;          // ❌ Error!..
* In expressions, byte/short/char promoted to int
 byte a = 10;
byte b = 20;
int c = a + b;           // ✅ Correct
// OR
byte c = (byte)(a + b);  // ✅ With casting

byte b = 10;
short s = 20;
int i = 30;
long l = 40L;

// What is result type?
b + s       // int
b + i       // int
i + l       // long
l + 2.5     // double
```
## MCQ Focus - Type Compatibility:

Q: Which requires explicit casting?
a) int to long  b) double to int ✅ c) byte to int  d) char to int

Q: What is output?
   byte a = 10, b = 20;
   byte c = a + b;
a) 30  b) Compilation error ✅ c) 0  d) Runtime error

Q: Type promotion: byte + short = ?
a) byte  b) short  c) int ✅ d) long

Q: Which is automatic conversion?
a) double to int  b) int to double ✅ c) long to int  d) float to int

Q: What happens: int x = 130; byte b = (byte)x;
a) b = 130  b) Data loss may occur ✅ c) Error  d) b = 0

* Short curcuit -> Logical Operator( && - both true , !! - ek bhi true)

## LOOP
1. // Infinite loop
for (;;) {
    // infinite
}
2. // No body
for (int i = 0; i < 5; i++);  // Just increments
3. For Each
   for (type variable : array/collection) {
    // loop body
}
Limitations:..

* Cannot modify array elements
* Cannot access index
* Only forward traversal

Q: switch can work with?
a) float  b) long  c) String ✅ d) boolean
Q: Enhanced for loop can?
a) Modify elements  b) Access index  c) Traverse forward only ✅ d) All

## Arrays
int[] nums = new int[5];     // {0, 0, 0, 0, 0}
double[] prices = new double[3];  // {0.0, 0.0, 0.0}
boolean[] flags = new boolean[4]; // {false, false, false, false}
String[] names = new String[3];   // {null, null, null}

### MCQ Focus - Arrays:
Q: Array index starts from?
a) 0  b) 1  c) -1  d) Depends
Q: arr.length is?
a) Method  b) Property  c) Variable  d) Function
Q: Default value of int array element?
a) null  b) 0  c) 1  d) undefined
Q: What is output?
int[] arr = {1, 2, 3};
System.out.println(arr[3]);
a) 3  b) 0  c) null  d) Exception
Q: 2-D array declaration?
a) int[][] arr;  b) int[,] arr;  c) int arr[][];  d) Both a and c
Q: Jagged array means?
a) Square matrix  b) Unequal columns  c) 3-D array  d) Sorted array
Q: Enhanced for loop can modify array?
a) Yes  b) No  c) Only 1-D  d) Only primitive
1 → a
2 → b
3 → b
4 → d
5 → d
6 → b
7 → b

* Memory Areas:

Heap: Objects, Instance variables..
Method Area: Static variables, Class metadata..
Stack: Local variables, Method calls..

Q5: if (x = 20) ❌

Tumhara: b (Nothing)..
Correct: c (Compilation error)..
Java mein: boolean context mein int nahi chal sakta (unlike C/C++)..

Q11: Unknown iterations loop ❌

Tumhara: b (while only)..
Correct: d (Both while and do-while)..

## OOPS
1. Class memory nahi lena --- Logical entity
2. object memory leta h  --- physical entity

## Abstract vs Interface
https://docs.google.com/document/d/1AJIemacjzREIiRbUp7hi0ZJM_1RmcdyA6KLAu0bkatI/edit?tab=t.0

```
class Demo {
    int x = 10;
    
    void display() {
        System.out.println("Display");
    }
}

public class Main {
    public static void main(String[] args) {
        Demo d1 = new Demo();
        d1.display();  // Display ✅
        
        Demo d2 = null;  // Null reference
        // d2.display();    // NullPointerException ❌
        
        if(d2 != null) {
            d2.display();  // Safe
        }
    }
}
```

## Comparison
1. Primitive Comparison (==):
```
int a = 10;
int b = 10;
System.out.println(a == b);  // true (values compare)
```
2. Reference Comparison (== vs equals):
```
String s1 = new String("Hello");
String s2 = new String("Hello");

System.out.println(s1 == s2);      // false (different objects)
System.out.println(s1.equals(s2)); // true (content same)

// String literals (special case)
String s3 = "Hello";
String s4 = "Hello";
System.out.println(s3 == s4);      // true (same object from pool)
```
## MCQ
```
Q: Static variable kitni baar create hota?
A: Ek baar (class load pe)

Q: Static method mein 'this' use kar sakte?
A: Nahi ❌

Q: main() method static kyun?
A: JVM bina object ke call kare
Q: Reference variable kaha store hota?
A: Stack

Q: Object kaha create hota?
A: Heap

Q: null reference ka kya matlab?
A: Kisi object ko point nahi kar raha

String s1 = null;
String s2 = null;

System.out.println(s1 == s2);      // ❓
System.out.println(s1.equals(s2)); // ❓
```

**Answer:**
```
s1 == s2           → true ✅ (both null)
s1.equals(s2)      → NullPointerException ❌

int[] a = {1, 2, 3};
int[] b = {1, 2, 3};

System.out.println(a == b);        // ❓
System.out.println(a.equals(b));   // ❓
```

**Answer:**
```
== → Reference compare, equals() → Content compare
a == b           → false ❌ (different objects)
a.equals(b)      → false ❌ (Object.equals checks reference)

// Content compare:
Arrays.equals(a, b)  → true ✅
```
```
10. Inheritance - Constructor Chain
javaclass A {
    A() { System.out.print("A"); }
}

class B extends A {
    B() { System.out.print("B"); }
}

class C extends B {
    C() { System.out.print("C"); }
}

public class Main {
    public static void main(String[] args) {
        C c = new C();
    }
}
Output: ABC ✅ (not CBA!)

-----------------
abstract class A {
    abstract void m1();       // ✅ OK
    // abstract void m2() { } // ❌ ERROR - body not allowed
}

class B extends A {
    // void m1() { }          // ❌ ERROR - must be public (or higher)
    public void m1() { }      // ✅ OK
}
```
```
class Student {
    String name;
    
    Student(String name) {
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {
        // Student s = new Student();  ❌ ERROR - no default constructor
        Student s = new Student("Rahul");  // ✅ OK
    }
}
```
1. Pass By value ----Primitives

```
public class Main {
    static void change(int x) {
        x = 100;
        System.out.println("Inside method: " + x);  // 100
    }
    
    public static void main(String[] args) {
        int a = 10;
        change(a);
        // Output: Inside method: 100
        
        System.out.println("Outside method: " + a);  // 10 (unchanged!)
    }
}
```

**Memory:**
```
Stack:
main() → a = 10
change() → x = 10 (copy)
         → x = 100 (local change)
         
a remains 10 ✅
```
2. Pass by Reference Value (Objects)
```
class Student {
    int marks;
}

public class Main {
    static void change(Student s) {
        s.marks = 100;
        System.out.println("Inside method: " + s.marks);  // 100
    }
    
    public static void main(String[] args) {
        Student s1 = new Student();
        s1.marks = 50;
        
        change(s1);
        // Output: Inside method: 100
        
        System.out.println("Outside method: " + s1.marks);  // 100 (changed!)
    }
}
```

**Memory:**
```
Stack:                  Heap:
main() → s1 → ──┐      ┌──────────┐
change() → s → ─┴─────→│ marks=100│
                        └──────────┘
Both point to SAME object!
```
## Association, Aggregation, Composition
https://docs.google.com/document/d/1AJIemacjzREIiRbUp7hi0ZJM_1RmcdyA6KLAu0bkatI/edit?tab=t.sw0f1bbugzka

## Diamond Problem solution
```
interface A {
    default void show() { System.out.println("A"); }
}

interface B {
    default void show() { System.out.println("B"); }
}

class C implements A, B {
    public void show() { // ✅ Override zaroori
        A.super.show(); // Specific interface call
    }
}
```
## Ypcasting/Downcasting
```
Upcasting automatic, Downcasting manual
instanceof se check karo before downcasting
Wrong downcasting = ClassCastException

```
## Enum
Special class for constants
```
enum Day {
    MONDAY, TUESDAY, WEDNESDAY // Constants
}

Day d = Day.MONDAY;
```
**Default ko package-private bhi bolte hain**
```
import java.util.ArrayList;
import java.util.*; // All classes in util

ArrayList<Integer> list = new ArrayList<>();
---------------------------------
import static java.lang.Math.PI;
import static java.lang.Math.*; // All static members

System.out.println(PI);      // Direct use (no Math.PI)
System.out.println(sqrt(4)); // Direct use (no Math.sqrt)
```
## Constructor Chaining
Ek constructor se dusra constructor call karna
Same Class (this)
```
javaclass Student {
    String name;
    int age;
    
    Student() {
        this("Unknown", 0); // Constructor call
    }
    
    Student(String name) {
        this(name, 18); // Constructor call
    }
    
    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```
Rules:

this() first line me hona chahiye
Ek constructor me sirf ek this() call
```
class A {
    A() {
        this(5);
        super(); // ❌ ERROR - dono ek sath nahi
    }
    A(int x) { }
}
```
## Protected Access Rule
```
Same package: Kisi bhi tarah access ✅
Different package: Sirf inheritance se ✅
Through parent object: ❌

// p1.Parent
package p1;
public class Parent {
    protected int x = 10;
}

// p2.Child
package p2;
import p1.Parent;
class Child extends Parent {
    void show() {
        System.out.println(x); // ✅ OK (inheritance)
        
        Parent p = new Parent();
        System.out.println(p.x); // ❌ ERROR
    }
}
-------------------------
// File1.java
package p1;
class A { // default class
    void show() { } // default method
}

// File2.java
package p2;
import p1.A; // ❌ ERROR - default class import nahi
```
## Requesting Garbage collector
1. System.gc(); or Runtime.getRuntime().gc() // GC ko request (suggestion)// Request hai, guarantee nahi
## finalize() Method
1. Object destroy hone se pehle ek baar call hota (cleanup activity)
2. 1 baar count hoga max
3. who call - GC thread
4. no garantee= call hoye na na
```
// A)
public void finalize() { } // ❌ public nahi (protected)

// B)
protected void finalize() throws Exception { } // ✅ OK

// C)
protected final void finalize() { } // ✅ OK (final allowed)

// D)
static void finalize() { } // ❌ static nahi
--------------------------------------------
Test t = new Test();
t = null;
System.gc();
t = new Test(); // Ye wala naya object
System.gc();
// finalize() maximum 2 baar (har object ke liye ek)
------------------------------------------------
class Node {
    Node next;
}
Node n1 = new Node();
Node n2 = new Node();
n1.next = n2;
n2.next = n1;
n1 = null;
n2 = null;
// Answer: 2 objects eligible (island)
--------------------------------
String s1 = new String("A");
String s2 = new String("B");
s1 = s2;
s2 = null;
// Answer: 1 ("A" object eligible)
```
## Wrapper Classes
Primitive types ko objects me convert karna...
char,boolean - parent class(object)
```
Integer i1 = 100;
Integer i2 = 100;
System.out.println(i1 == i2); // ✅ true (cache)

Integer i3 = 200;
Integer i4 = 200;
System.out.println(i3 == i4); // ❌ false (no cache)
System.out.println(a.equals(b));   // true
 Cache Range: -128 to 127 (constant pool)
```
```
StringBuffer sb = new StringBuffer("Hello");

// Append (add at end)
sb.append(" World"); // "Hello World"

// Insert
sb.insert(5, " Java"); // "Hello Java World"

// Delete
sb.delete(5, 10); // "Hello World"

// Replace
sb.replace(0, 5, "Hi"); // "Hi World"

// Reverse
sb.reverse(); // "dlroW iH"

// Capacity
sb.capacity(); // Default: 16 + length

// Multi-threading
StringBuffer sb = new StringBuffer(); // ✅ Thread-safe

// Single thread
StringBuilder sb = new StringBuilder(); // ✅ Faster

```
## Object Class
class Student { } 
// Internally: class Student extends Object { }
1. toString() Method   -- println(object) internally toString() call karta

```
deafult
class Student {
    int id;
    String name;
}

Student s = new Student();
System.out.println(s); // Student@15db9742 (classname@hashcode)
System.out.println(s.toString()); // Same
```
2. equals() method
```
Student s1 = new Student(1, "Ram");
Student s2 = new Student(1, "Ram");

System.out.println(s1 == s2);        // false (reference compare)
System.out.println(s1.equals(s2));   // false (default = ==)
```
## data & calendar -- java.util.data
  ```
--------------------------
override string
class Student {
    int id;
    String name;
    
    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }
    
    @Override
    public String toString() {
        return "Student[id=" + id + ", name=" + name + "]";
    }
}

Student s = new Student(1, "Ram");
System.out.println(s); // Student[id=1, name=Ram]

Calendar cal = Calendar.getInstance();
cal.set(Calendar.MONTH, 0); // January (0-based)
```
## Thread
1. join
```
public class Main {
    public static void main(String[] args) {
        Thread t1 = new Thread(() -> {
            for(int i = 1; i <= 5; i++) {
                System.out.println("Thread-1: " + i);
                try { Thread.sleep(500); } 
                catch(InterruptedException e) { }
            }
        });
        
        t1.start();
        
        try {
            t1.join();  // Main waits for t1 to finish
        } catch(InterruptedException e) {
            e.printStackTrace();
        }
        
        System.out.println("Main thread finished");
    }
}
```

**Output:**
```
Thread-1: 1
Thread-1: 2
Thread-1: 3
Thread-1: 4
Thread-1: 5
Main thread finished  ← Prints AFTER t1 completes
```

```
public class Main {
    public static void main(String[] args) {
        // Main thread priority = 5
        
        Thread t1 = new Thread(() -> {
            System.out.println("T1: " + 
                Thread.currentThread().getPriority());
        });
        
        t1.start();  // T1 inherits priority 5 from main
    }
}
```
```
class Shared {
    synchronized void consume() throws InterruptedException {
        System.out.println("Waiting...");
        wait(); // Release lock and wait
        System.out.println("Resumed");
    }
    
    synchronized void produce() {
        System.out.println("Producing...");
        notify(); // Wake up one waiting thread
    }
}

Shared s = new Shared();

// Thread 1
new Thread(() -> {
    try { s.consume(); } catch(Exception e) {}
}).start();

Thread.sleep(1000);

// Thread 2
new Thread(() -> s.produce()).start();

// Output:
// Waiting...
// Producing...
// Resumed
```
```
void method() {
    wait(); // ❌ IllegalMonitorStateException (no synchronized)
}

synchronized void method() {
    wait(); // ✅ OK
}
```
## 5. Generics Introduction
Type-safe collections - compile time pe type check
```
ArrayList<String> list = new ArrayList<String>();
list.add("Java");
list.add(10); // ❌ Compile error (type safe)

String s = list.get(0); // No casting needed
------------------------
without
ArrayList list = new ArrayList();
list.add("Java");
list.add(10); // ✅ Allowed (Object type)

String s = (String) list.get(0); // Manual casting
String x = (String) list.get(1); // ❌ Runtime error (ClassCastException)
```
```
class Util {
    // Generic method
    static <T> void print(T item) {
        System.out.println(item);
    }
    
    // Generic with return
    static <T> T getFirst(T[] arr) {
        return arr[0];
    }
}

// Usage
Util.print("Java");   // T = String
Util.print(100);      // T = Integer

String[] arr = {"A", "B"};
String first = Util.getFirst(arr);
```
MCQ Trap
```
<T> void method(T item) { } // ✅ Generic method

void method(T item) { }     // ❌ T undefined (not generic)
```
## Wildcards
Unknown type represent karna  -- ?
```
void print(List<?> list) { // Any type
    for(Object obj : list) {
        System.out.println(obj);
    }
}

List<String> strList = new ArrayList<>();
List<Integer> intList = new ArrayList<>();
print(strList); // ✅
print(intList); // ✅
```
##  Metadata
Data about data - extra information about code
```
java@Override    // Metadata
@Deprecated  // Metadata
@SuppressWarnings("unchecked")
----------------------------------
Built-in Annotations:

@Override - Method override check
@Deprecated - Old/outdated feature
@SuppressWarnings - Warning ignore
@FunctionalInterface - Single abstract method
```
MCQ
```
synchronized void method() { }
// Lock kis pe? → this (object)

synchronized static void method() { }
// Lock kis pe? → Class
---------------------------------------
void method() {
    wait(); // ❌ IllegalMonitorStateException
}

synchronized void method() {
    wait(); // ✅ OK
}
-------------------------------
List<Integer> list = new ArrayList<>();
list.add(10);
list.add("Java"); // ❌ Compile error (type safe)
---------------------------------------
List<? extends Number> list = new ArrayList<Integer>();
list.add(10); // ❌ Cannot add  // Isme compile-time error aayega ✅

List<? super Integer> list = new ArrayList<Number>();
list.add(10); // ✅ Can add
-------------------------------------
Class<?> c = String.class;
System.out.println(c.getName()); // java.lang.String
```
HINT
```

## **Quick Formula Sheet**

### **Synchronization**
- Method = Lock on **object** (this)
- Static method = Lock on **Class**
- Block = Lock on **specified object**
==========================================
### **wait/notify**
- `wait()` = Release lock + WAIT state
- `notify()` = Wake one thread
- `notifyAll()` = Wake all threads
- **synchronized block/method me hi** use
====================================
### **Generics**
- `<T>` = Type parameter
- Type safety + No casting
- Runtime pe type **erase** (type erasure)
=============================================
### **Wildcards**

? extends T → Read (Producer)
? super T   → Write (Consumer)
?           → Read as Object
```
