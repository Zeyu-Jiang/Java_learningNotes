#Concepts about JVM#
**JVM, JRE, JDK**
*JVM*: is virtual machine and provides runtime environment. 
*JVM* performs main tasks
    loads code
    verifies code
    executes code
    prvoides runtime environment
*JRE* is used to provide runtime environment. It is the implementation of *JVM*.
It contains set of libraries and other files that *JVM* uses at runtime.
*JDK* contains *JRE* and development tools.

**Internal Architechure of JVM**
*1. classloader*: is a subsystem of *jvm* that uses to load class files.
*2. memory area*
    *class area*: stores per-class structures such as constant pool, field, method data and the code for methods.
    *heap area*: stores objects.
    *stack area*: stores frames. It holds local variables and partial results. plays a part in method invocation an return.
    *program counter register*: contains the address of the *JVM* instruction currently being executed.
*3. execution engine*
virtual processor
interpreter
just-in-time compiler