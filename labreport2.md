# StringServer - Isabelle Layon
## Code for StringServer

## Using /add-message
> Try #1

* The StringServer's main method is first called, in order to read the terminal input `java StringServer 4000` and start a new local server with port 4000.
In order to add "Hello" to string, the handleRequest method takes in the URL, checks if the path contains `"/add-message"`, and checks if there is the query contains `"="`.
If there is an `"s"` after the `"="`, then a string will be added.
* The port number, which is args[0] inside String[] args, is a relevent argument for the main method, as it becomes the local port used for a StringServer.
The relevant argument for handleRequest is a URI url, which the method checks to see if the url contains `/add-message`. It will return `"404 Not Found!"` elsewise.
handleRequest also checks the url for an `"="` and `"s"` in the query.
*String myString is a relevant field of the class, and is intialized as an empty String inside of the Handler class.
*After this request, the value of myString has been updated to "Hello". `/n` was not used while updating the value of myString, since myString was initially empty.

> Try #2

* We do not need to start a new local server, so the main method is not called. The handleRequest method takes in the new URL, and adds the String "Have a nice week!",
after checking the path and query.
* The URI url is the relevant argument for handleRequest, which checks the path and query similar to Try #1. String myString is the relevant field of the class,
and its value before the request is "Hello".
* After this request, the value of myString has been updated to "Hello" + '\n' + "Have a nice week!", which displays as:

```
Hello 
Have a nice week!
```

when on the local StringServer.

## Lab 3 Bug: 

> Inputs
* A failure inducing input for the program would be the Junit test

```
@Test
public void testReversedWithMoreElements() {
  int[] input1 = { 4, 5, 6 };
  assertArrayEquals(new int[]{ 6, 5, 4 }, ArrayExamples.reversed(input1));
 }
 ```
 
 * A non-failure inducing input for the program would be the Junit test
 
 ```
 @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
  ```
 > Symptom
 * Failure inducing input:

 * Non Failure inducing input:

 > Bug 
 * Before fixing:
 ```
 for(int i = 0; i < arr.length; i++){
  arr[i] = newArray[arr.length - i - 1];
 }
 return arr;
 ```
 
 * After fixing:
 ```
 for(int i = 0; i < arr.length; i++){
  newArray[i] = arr[arr.length - i - 1];
 }
 return newArray;
 ```
 
 * `arr[i]` is changed into `newArray[i]` in order for each index in the new reversed array to be proper updated. 
 ``newArray[arr.length - i - 1]`` is changed into ``arr[arr.length - i - 1]`` so that the empty newArray is being updated with the values from the intial array,
 rather than attempting to update the intial array with empty values from newArray. Finally, the updated newArray is returned instead of the initial array.

## What I Learned in Week 3
* During week 3, I learned the definitions of symptoms and failure-inducing inputs, along with how to identify or create failure-inducing inputs and
how to identify symptoms in a Java program. A failure-inducing input is an input that, when tested, causes a program to produce an error, such as when an
array containing elements produced an error for the reversed method. A sympton is the behaviors exhibited by a program, which could be intended (ie. what is displayed
in a website), or could be the results of a bug in the program (ie. an IndexOutOfBounds error).
