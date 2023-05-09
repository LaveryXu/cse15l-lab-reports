## the code for my StringServer:
[StringServer.java](StringServer.java)
## two screenshots of using /add-message.
- ![myString](myString.png)
  - Which methods in my code are called?
    - At first, the **main** method is run and **parseInt** method is called with the argument, 7777, which is the port number I entered in the terminal). The StringHandler class's int field, *portNum*, is then assigned the int value, 7777, that the parseInt method returns. Then the **start** method in Server.java is called with arguments portNum the field and an instance of StringHandler the class (this instance is returned by StringHandler's constructor via calling the constructor with the arugmment, portNum the field). During the execution of the start method, the **handleRequest** method is called and recognize that the initial url's path is /, therefore prints out texts that instruct the user to input texts they want to print on the webpage. After the String, myString, is entered in the instructed format, handleRequest extracts the user's input String and concatenate the user's String to the class StringHandler's field *x*, which is initialized as an empty String. At last, the handleRequest method returns a String by making the method call, String.**format**(x) and the user's input String, myString, is printed on the webpage.

- ![YouTube](YouTube.png)
  - Which methods in your code are called?
    - The main method, the parseInt method, the start method, . The field portNum, .
  - What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  - How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

By values, we mean specific Strings, ints, URIs, and so on. "abc" is a value, 456 is a value, new URI("http://...") is a value, and so on.)
