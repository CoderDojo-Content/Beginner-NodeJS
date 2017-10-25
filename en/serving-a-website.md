1. Serving a website as a string is all well and good for something simple, But if you have more than 5 lines of code it would become very messy, Thats why express has _static file serving_.
2. Replace this:

   ```js
        app.get('/', function (req, res) {
            res.send('Hello World!')
        });
   ```

   With this:

   ```js
        app.use(express.static('public'))
   ```

3. Now create a folder\( In the same place as your program \) called "public" and create a [simple html website](https://www.gitbook.com/book/coderdojo/beginner-html-css/details) called _index.html_.

4. Restart your program and reload your browser, Hopefully you see your brand new website!

5. So you have gotten a basic web server, But you are probably wondering what the point of programming it is, Why not just download a web-server to host your website?
6. As you may have seen in the Javascript tutorial, You can store things in the users browser, But thats not much good if you need to share things. Think about Facebook, How does that work? Well, Your computer sends a message with your post to the Facebook server, Which stores that post\( In a database. \). And then, When all your friends computers ask for an update, The Facebook server sends them your post.

7. We are going to create a website that counts how many times a button has been clicked _on any computer looking at your website._ To do this we are going to make an _API_.  



