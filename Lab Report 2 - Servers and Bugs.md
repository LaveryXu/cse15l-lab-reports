# Servers and Bugs
## Part 1
The code for my StringServer is [here](StringServer.java).

2 screenshots of using /add-message:
- ![myString](myString.png)
  - At first, the `main` method is run (called with the argument, **7777**) and `parseInt` method is called with the argument, **7777**, which is the port number I entered in the terminal). The StringHandler class's int field, `portNum`, is then assigned the int value, **7777**, that the parseInt method returns. Then the `start` method in Server.java is called with arguments **portNum** the field and **an instance of StringHandler the class** (this instance is returned by StringHandler's constructor via calling the constructor with the arugmment, portNum the field). During the execution of the start method, the `handleRequest` method is called with the argument that's the entire url of the webpage, **http://localhost:7777/**, and recognizes that the initial url's path is /, therefore prints out texts that instruct the user to input texts they want to print on the webpage. After the String, **"myString"**, is entered in the instructed format, handleRequest is again called with the updated url of the webpage, **http://localhost:7777/add-message?=myString**, and extracts the user's input String and concatenate the user's String to the class StringHandler's field `x`, which is **initialized as an empty String**. At last, the handleRequest method returns a String by making the method call, String.`format(x)` and the user's input String, **"myString"**, is printed on the webpage.
- ![YouTube](YouTube.png)
  - The `main` method, the `parseInt` method, and the `start` method are called in the previous screenshot. The `handleRequest` method is again called with the argument, the entire url that's **http://localhost:7777/add-message?=https://www.youtube.com/** in this screeshot and contatenate the user's String, **https://www.youtube.com/** to the field `x`. Therefore, field `x` is now this String: "myString\n2023\nhttps://www.youtube.com/". Then `handleRequest` method returns a String by making the method call, `String.format(x)`, and the returned String, **myString\n2023\nhttps://www.youtube.com/** is printed on the webpage. The field `portNum` is not changed and remians **7777**.

## Part 2
the buggy method I choose from lab 3 is `static int[] reversed(int[] arr)` in `ArrayExamples.java`, as shown below:
```
// Returns a *new* array with all the elements of the input array in reversed 
// order
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
```

- A failure-inducing input for `static int[] reversed(int[] arr)`: {1,2,3,4,5,6}
  - as a JUnit test and any associated code (write it as a code block in Markdown):
    ```
    int[] input2 = {1,2,3,4,5,6};
    assertArrayEquals(new int[]{6,5,4,3,2,1}, ArrayExamples.reversed(input2)); // failure #1
  ```
- An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
- The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
- The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
- Briefly describe why the fix addresses the issue.

## Part 3
a question that I have: how do I make an entire paragraph or code block a single bullet point in Markdown?