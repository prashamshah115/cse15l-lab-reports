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





**Screenshot 2**


## Part 2

## Part 3 
