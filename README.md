# Group-Chatting-Application-using-JAVA

It's a Desktop Application that allows group chat in a Client-Server Network.

This project is made using java, more specifically, Swing, Socket Programming and concept of Multithreading.

## How does this project works ?

1. Server code is started first and then multiple clients can run their code.

2. On Server side, as soon as a client request arrives, it assigns one thread acting as a server thread for only that single client, thus one to one relationship between server thread and client comes into picture which exists till client signs out from the group chat.

3. Server also assigns separate socket, data input and output streams to all server threads.

4. An ArrayList is maintained which consists of all the active server threads, used to broadcast messages to all online users. 

5. On Client side, there is a requirement of 2 separate threads for reading and writing (sending) messages as both processes can't be completed using a single thread.

6. As soon as a client signs out (closes the window), its corresponding server thread is removed from the ArrayList and all the active streams and socket of client and corresponding server thread are closed, also all respective threads stops.
