# Fabian (Read document carefully to perform actions)


### 1. Training the NLU model

Training of the NLU model using command line interpreter:   

``` rasa nlu train ```

### 3. Training the Rasa model: 

1. Start the custom action server if we have any custome action available in the project by running:  

``` rasa run actions ```  

2. Open a new terminal and train the Rasa Core model by running:  

``` rasa train```  

if the error occures like "Addressed is already in Used with some port number like ex. 5055/8000 etc" or CannotListenError: Couldn't listen on 0.0.0.0:5005:Address already in use.
then run:

'''lsof -ti:5005 | xargs kill -9''' # To kill the running port by changing port number


### 4. Starting the online training session(Interactive Learning):
Using Interactive learning, we can create a meaningfull stories and generate a own training phrases so that we can add this into training file and storty file.

The process of running the online session is very similar to training the Rasa Core model or interactive learning:
1. Make sure the custom actions server is running:  

``` rasa run actions ```   # Where, [actions] is the name of python code file.i.e actions.py

2. Start the online training session by running:  

``` rasa interactive ``` 

     OR


``` rasa x ```


### 5. Run server : 

1. Go to folder ``` Chatbot-Widget``` which is running using socketio. And open ```index.html``` file using browser.

  
