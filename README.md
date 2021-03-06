## Chat Application

### Functionalities
1.Room Creation 2.User Authentication(JWT) 3.Chat(Socket.io) 4.Database(MongoDB) 5.Dark/Light Mode 

#### Room Creation
Authentic user is able to create a room or join an existing room.User only need to type in unique room name in order to create a room.Room creation is handled in the server side .Room name is saved into mongoDB database which generates an id for each room which is later used for users to join the room using socket.io.

#### User Authentication
User Authentication and Authorization is done with the help of Javascript Web Token(JWT) implemented in the server side which stores the email and hashed password in MongoDB database and generates access token to use the application for the authentic user.

#### Chat
Authentic user upon joining the room is provided with a unique socketId which is same as the id generated by mongoDB for every unique user saved in the database and multiple users that join the same room are notified of the other users that have joined the room and are able to chat with one another in real time using socket.io message emit feature.
Users can leave and again join the same room.Users are notified of other users joining and leaving room.

#### Database
MongoDB database is used to store the user email,hash password along room names and messages that are exchaged in between users but those old messages are not used to display the message in the room rather message during a chat session is used so when all uses leave and same room is joined again old messages are not displayed.MongoDB database is implemented in the server side using mongoose.

#### Dark/Light Mode
A toggle switch to switch in between dark and light mode is present which is implemented using Material UI themes.
