1. We are going to make the most basic web-server possible. First of all, Type this in to the editor:

   ```js
    var express = require('express')
    var app = express()
   ```

   What we just did was import express and set it up.

2. Next we are going to set up a _route_, We are going to set up the default "/" route.

   ```js
   app.get('/', function (req, res) {
       res.send('Hello World!')
   });
   ```

3. Now we are going to tell the web-server to listen on port 3000.

   ```js
   app.listen(3000, function () {
       console.log('Example app listening on port 3000!')
   });
   ```

4. Finally to run the code, Type this into the command prompt:

   ```
      node main.js
   ```

   Then go to _127.0.0.1:3000_ in your web-browser. This is the IP address used to access your own computer, Alternatively, You may be able to type _localhost:3000_. Hopefully you see "Hello World!".

5. What just happened was that your web-browser asked for the code and your program returned "Hello World!", If you had returned the HTML code of a website, Your browser would have rendered the website!

\*You might be wondering why you had to put _:3000_ at the end of your ip address, 3000 is the port number, If you dont put in a port number, .E.G. Facebook.com your browser tries port 80. Unfortunately, To access port 80 you need super user access, Which is tricky on windows. However, If you are using a Mac or Linux machine, Feel free to change the port number to 80 and run this command instead:

```bash
sudo node main.js
```



