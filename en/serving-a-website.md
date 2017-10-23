1. Serving a website as a string is all well and good for something simple, But if you have more than 5 lines of code it would become very messy, Thats why express has _static file serving_.
2. Replace this:

   ```
        app.get('/', function (req, res) {
            res.send('Hello World!')
        });
   ```

   With this:

   ```
        app.use(express.static('public'))
   ```

3. Now create a folder\( In the same place as your program \) and create a [simple html website](https://www.gitbook.com/book/coderdojo/beginner-html-css/details) called _index.html_.

4. Restart your program and reload your browser, Hopefully you see your brand new website! 



