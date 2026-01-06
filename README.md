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
