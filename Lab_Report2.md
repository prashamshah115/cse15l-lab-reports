# PRASHAM'S LAB REPORT 2 

## Part 1

**My code for ChatServer**

```
import java.io.IOException;
import java.net.URI;

class ChatHandler implements URLHandler {
    private StringBuilder chatMessages = new StringBuilder(); //idk googled what data structure would be best-suited `

    @Override
    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            String messageParam = null;
            String userParam = null;

            for (String param : parameters) {
                String[] keyValue = param.split("=");
                if (keyValue.length == 2) {
                    if (keyValue[0].equals("s")) {
                        messageParam = keyValue[1];
                    } else if (keyValue[0].equals("user")) {
                        userParam = keyValue[1];
                    }
                }
            }

            if (messageParam != null && userParam != null) {
                String newChatMessage = userParam + ": " + messageParam + "\n";
                chatMessages.append(newChatMessage);

                
                return chatMessages.toString();
            } else {
               
                return "400 Bad Request!";
            }
        } else {
            
            return "404 Not Found!";
        }
    }
}

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new ChatHandler());
    }
}

```
**Screenshot 1**

<img width="1043" alt="Untitled" src="https://github.com/prashamshah115/cse15l-lab-reports/assets/155808867/3e182fb5-b466-4760-bfff-fb80d4ec910c">

In this case, we can use the 'curl' command.
`curl "http://localhost:8080/add-message?s=Hello&user=pshah"`

Here, the Handler method in ChatHandler is called. The relevant arguments to this method are an URI object representing the URL "http://localhost:4000/add-message?s=Hello&user=pshah".
The values of the relevant fields, chatMessages before the request: Empty StringBuilder; chatMessages after the request: "jpolitz: Hello\n".
The chatMessages field is updated with a new chat message.


**Screenshot 2**

<img width="1043" alt="Untitled 2" src="https://github.com/prashamshah115/cse15l-lab-reports/assets/155808867/7a6ddf18-8550-4224-98c0-a607f574ef6f">

In this case, we can use the 'curl' command.
`curl "http://localhost:8080/add-message?s=How%20are%20You&user=ronaldo"`

Here, the Handler method in ChatHandler is called. The relevant arguments to this method are an URI object representing the URL "http://localhost:4000/add-message?s=How%20are%20You&user=ronaldo".
The values of the relevant fields, chatMessages before the request: "pshah: Hello\n"; chatMessages after the request: "pshah: Hello\nronaldo: How are you\n".
The chatMessages field is further updated with a new chat message.


## Part 2

**Screenshot of the absolute path to the private key for my SSH key for logging into ieng6**


**Screenshot of the absolute path to the public key for your SSH key for logging into ieng6**

<img width="601" alt="prasham" src="https://github.com/prashamshah115/cse15l-lab-reports/assets/155808867/9769b8da-ee33-4b47-98f5-9c15645f788c">


**Screenshot of terminal interactions where I log into my ieng6 account without being asked for a password.**

<img width="869" alt="terminal interaction" src="https://github.com/prashamshah115/cse15l-lab-reports/assets/155808867/e53293ac-c29b-437a-bb6e-66384dab7b16">



## Part 3 

There's been quite a few concepts and ideas that I have been introduced to so far in this class, that I was not aware of before. This includes knowledge of Java remote servers - the concept of accessing said web servers through a remote device has proved quite interesting to me. Further, I had always seen 'README.md' files in github repos, but only recently I learned that they were fundamentally files containing the commands which are run. Further, I have been introduced to why and how the terminal is used.
