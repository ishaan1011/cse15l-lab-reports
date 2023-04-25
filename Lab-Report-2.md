# Lab Report 2 - Servers and Bugs

## PART 1: Creating a Web Server (StringServer)
We need to create a web server called "StringServer" that keeps track of a single string that gets added to by incoming requests.

The code for StringServer.java is given below:

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String str = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            if (str.isEmpty()){
                return "String is empty.No message added yet.";
            }
            else{ return str;
            }
        }
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                str+=parameters[1]+"\n"; return str;
            }
        }
        return "404 Not Found!";
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

The effect of this code is to concatenate a new line (\n) and the string after '=' to the running string, and then respond with the entire string so far.
We can run this code by entering:
* `javac Server.java StringServer.java`
* `java StringServer 4000`
When the code compiles and runs, we will be able to see `Server Started! Visit http://localhost:4000 to visit.` on our terminal.

The page displayed after running this should look like:

![Image](empty.png)

Now we can use the "/add-message" to add text to our webpage. The webpage would look like:

![Image](hello.png)

In the above image, when we succeed the url with “/add-message?s=Hello”,the server displays "Hello".

Next, when we add “Hi”, it displays "Hello" and "Hi" in different lines.

![Image](hi.png)

## Step 2: Remotely Connecting
