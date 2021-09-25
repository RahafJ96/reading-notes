# Java Basics

## Language Basics
### Variables
Java programming language defines the following kinds of variables:
 1. Instance Variables (Non-Static Fields)
 2. Class Variables (Static Fields)
 3. Local Variables
 4. Parameters

### Naming Variables
 1. Variable names are case-sensitive. A variable's name can be any legal identifier — an unlimited-length sequence of Unicode letters and digits, beginning with a letter, the dollar sign "$", or the underscore character "_". The convention, however, is to always begin your variable names with a letter, not "$" or "_".
 2. Subsequent characters may be letters, digits, dollar signs, or underscore characters.
 3. If the name you choose consists of only one word, spell that word in all lowercase letters. If it consists of more than one word, capitalize the first letter of each subsequent word. 

### Operators
- postfix:	`expr++ expr--`
- unary:	`++expr --expr +expr -expr ~ !`
- multiplicative:	`* / %`
- additive:	`+ -`
- shift:	`<< >> >>>`
- relational:	`< > <= >= instanceof`
- equality:	`== !=`
- bitwise AND:`	&`
- bitwise exclusive OR:	`^`
- bitwise inclusive OR:	`|`
- logical AND:	`&&`
- logical OR:	`||`
- ternary:	`? :`
- assignment:	`= += -= *= /= %= &= ^= |= <<= >>= >>>=`

### Expressions, Statements
- An expression is a construct made up of variables, operators, and method invocations, which are constructed according to the syntax of the language, that evaluates to a single value. You've already seen examples of expressions, illustrated in bold below.
** Example **:
`x + y / 100`
- Statements are roughly equivalent to sentences in natural languages. A statement forms a complete unit of execution. The following types of expressions can be made into a statement by terminating the expression with a semicolon (;).

**Example**:
`System.out.println("Hello World!");`

### Control Flow Statement
The statements inside your source files are generally executed from top to bottom, in the order that they appear. Control flow statements, however, break up the flow of execution by employing decision making, looping, and branching, enabling your program to conditionally execute particular blocks of code.
This section describes the decision-making statements (if-then, if-then-else, switch), the looping statements (for, while, do-while), and the branching statements (break, continue, return) supported by the Java programming language.


 [Java Basics](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html)