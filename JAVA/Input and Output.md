## Scanner
**Reading a file**
To begin, construct a File object with the name of the input file:
```java
File inputFile = new File("input.txt");
```
Then use the File object to construct a Scanner object:
```java
Scanner in = new Scanner(inputFile);
```
This **Scanner** object reads text from the file input.txt. You can use the Scanner methods
(such as nextInt, next Double, and next) to read data from the input file.
For example, you can use the following loop to process numbers in the input file:
```java
while (in.hasNextDouble()) {
	double value = in.nextDouble();
	Process value.
}
```
To write output to a file, you construct a **PrintWriter** object with the desired file name,
for example
```java
PrintWriter out = new PrintWriter("output.txt");
```

## Formatting output
```java
System.out.printf("%-10s%10.2f", items[i] + ":", prices[i]);
```
![](Pasted%20image%2020220620230042.png)

## Exception handling
There are two aspects to dealing with exceptions: detection and handling.

## Errors
**Runtime error:
- The JVM detects the error while the program is running. To handle these errors we can apply exception handling.
**Compile time error:
- The compiler detects the errors, the program is unable to run because of something incorrect (missing semicolon, bracket, class not found, etc).