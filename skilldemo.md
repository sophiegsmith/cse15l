# SKILL DEMO NOTES

**Step 1: Cloning the Repository**
- command to clone repositor: `git clone <url>`
- command to change directory: `cd <name>`

**Step 2: Edit the testscript**
editing the `test.sh` file
- in the test.sh file currently
    ```
    set -e

    javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java

    # java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore 
    ```
- to edit: 
```
#!/bin/bash
set -e

# Compile the Java files, including the ChatServer and HandlerTests
javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar ChatServer.java HandlerTests.java

# Run the HandlerTests and capture the output
java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore HandlerTests  
```

**Step 3: Compile and run tests for ChatServer**
- 1 should fail
- how to run test.sh script:
    - make sure its executable and run command: `chmod +x test.sh`
    - after its made executable run command: `./test.sh`
    - this will compile the java files and run the texsts as specified in script content

**Step 4: Edit test files to fix test input**
- note: errors are in the second test
- also notice: `String url = "http://localhost:4000/chat?name=edwin&message=happy%20friday!";`
- edit to inset `user`

**Step 5: Rerun tests**
- place output in proper txt file

**Step 6: Compile and run the ChatSert**
- command to compile: `javac Server.java ChatServer.java`
- command to run: `java ChatServer 4000`
- open up the browser

**Step 7: Load the path `chat` on the query**
- to do this the line is: `/chat?user=onat&message=hi`
- output should be:
  ```
  onat : hi
  ```

**Step 8: Change the code to add a case for the root path `/`**
- adding a case for root path `/`:
  ```
  // Handle request to root path and return all chat messages so far
        if (url.getPath().equals("/")) {
            return this.chatHistory; // Return the current chat history
        }
  ```

**Step 9: Recompile and restart the server**
- after changes server restarted fine
- used 4000

**Step 10: Load the path `/chat` on that server**
- case with user = joe and message = hi
- output should be:
  ```
  joe: hi
  ```

**Step 11: Repeat step 10**
- case with user = onat and messge = hi
- output should be:
  ```
  joe: hi

  onat: hi
  ```

**Step 12: Load the root `/` path in the server**
- use root path `/`
- output should be:
  ```
  joe: hi

  onat: hi
  ```

**Step 13: copy output of loading that root path**
- place it in the corresponding txt file
- look above at **step 12**

**Extra Notes**
- write a new test method for a URL path:
```
```

- run the test method:
```
```

- write a method for root path:
```
```