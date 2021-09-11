# Design Facebook messenger

Use a main chat api to handle messages
Use websockets for chat
use loadbalancer for the chat api with multiple instances for the chat api.
Now we have a distributed system, so we need a way for each chat api instance to talk to each other.
We can solve this with a publish/subscribe function.
Use a Message service queue to handle this. When a new message comes in, the chat api publishes to the queue. Then the message service will send the message to the user subscribed to that message.
Database: Needs to support a large volume of messages and needs high availability. Consistency is not important to a message service. NoSQL would be best here as it can handle DB sharding easier.


lead an effort a chat application. biult with ruby on rails. we want to launch it in 3 months. hasn't been tested in production. Feature complete
expect 10 million users on day 1. 
1. WHat are the pieces to get it deployed to a cloud? website
2. Who are the team members going to be, SRE etc. 
3. What is the timeline?
   in 2 months in staging
   in 1 month, build in docker.
   can we do things concurrently.

Need a load balancer
multiple instances of app
2 env, staging and production
Cloud provider: DCOS
postgresql database - 

## user table
email address 
userid, 

## messages table
id, from_user_id, to_user_id, message, timestamp


  
keytool -genkey -v -keystore c:\Users\johnn\upload-keystore.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias upload
