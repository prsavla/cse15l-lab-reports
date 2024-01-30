# Lab Report 2 - Servers and SSH Keys (Week 3)
## Pratham Savla

### Part 1:
Code For Chat Server:

![Code For Chat Server](part1.png)

Two Screenshots Of Using Add Message:
![Using Add Message #1](part2.png)
Methods that are called in the code: Primarily, when the user first types in `localhost:4001/` the `handleRequest` method is called which performs different actions depending on the path provided. If a single `/` is present as the path, the program simply outputs the chat log. If   `/add-message` is provided as the path with queries such as `/add-message?s=Hello&user=jpolitz`, then the "Hello" from user jpolitz is added to the Chat Log. Helper methods like .getPath(), .contains, .substring, .indexOf, .getQuery are all used to assist in extracting the right fields from the query. 

Arguments to the methods: The main argument to `handleRequest` is a URI object which contains the URL that the user types in. The argument to the .contains() method is `/add-message` to check if that is the path provided by the user. 

How the values change: The main value that changes is the String chatLog to reflect the messages added by the users of the program. One of the main issues I was having with my code is that I declared the String variable chatLog inside of the handleRequest method which caused chatLog to never update with a new message each time `/add-message` was called. I now understand that chatLog has to be declared outside of the `handleRequest` method. 

![Using Add Message #2](part3.png)
Methods that are called in the code: Similar to the first screenshot, when the user types in `local

### Part 2:

Absolute path to my private key for logging into ieng6:
![Private Key](part5.png)

Absolute path to my public key for logging into ieng6:
![Public Key](part4.png)

Logging into my ieng6 server without being asked for password:
![No password](part6.png)

### Part 3:
There were many new things that I learned in both the labs from week 2 and week 3. I'm beginning to understand and wrap my head around the idea of a web server a lot more. This was one of the first times in my life using commands like `ssh` to access a web server or commands like `scp` for securely transferring files onto a web server. The whole idea of making a ChatServer was mind-blowing because we had essentially created a web-based application for the first time in class. We could technically acess other people's ChatServers if they were running on ieng6.ucsd.edu.


