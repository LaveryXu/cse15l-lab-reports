## the code for my StringServer:
[StringServer.java](StringServer.java)
## two screenshots of using /add-message.
- ![myString](myString.png)
  - Which methods in your code are called?
    - At first, the main method is run and parseInt method is called and with the argument being 7777, the port number entered by the user (me in this case). The StringHandler class's int field, portNum, is assigned the int value, 7777, that parseInt method returns. Then the start method in Server.java is called with arguments portNum the field and an instance of StringHandler the class (this instance is returned by StringHandler's constructor via calling the constructor with the arugmment portNum the field).
  - What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  - How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

- ![YouTube](YouTube.png)
  - Which methods in your code are called?
  - What are the relevant arguments to those methods, and the values of any relevant fields of the class?
  - How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

By values, we mean specific Strings, ints, URIs, and so on. "abc" is a value, 456 is a value, new URI("http://...") is a value, and so on.)
