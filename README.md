# Alexa's Adventure
Game which allows you to interact with the story. Each scene in a story is saved as a number in DynamoDB. When a user starts the game again, this number is pulled from Dynamo DB so that the game knows where to start playing from. Game is also able to play sounds from S3. 

# YouTube Demo
https://youtu.be/JI9Q9LvhG7Q

# Architecture Diagram
Users speak to Alexa. This sends JSON to a lambda function which processes it (Pulling saves from DynamoDB, moving along users to a new scene, etc.). Some events in the story cause audio to be played which is stored on S3. Lambda function returns JSON which contains SSML Alexa processes to speak.
![alt text](https://s3.amazonaws.com/media-p.slid.es/uploads/783361/images/4299080/Web_App_Reference_Architecture__1_.png)

# Configuration Steps 
