1. Although we went to our API directly with the browser, Normally your code would use the API in the background when a user preforms an action, .E.G. Presses a button.
2. Make a simple website with a piece of text in the middle and a button under it. Alternatively, You can use [this one I pre-made.](https://gist.github.com/HarveyBrezinaConniffe/d217fa01d978cc53268c56a7db0d560a) 
3. Right now it just alerts you when the button is pressed. Replace the alert with some code to make a request to your API.\* If you need help remembering how to do that, Go back to the [advanced javascript tutorial.](https://www.gitbook.com/book/coderdojo/advanced-javascript-sushi/details)
4. Now reload your page and press the button! \( Hopefully your program prints out "Button pressed!". \)
5. The number on the page still says 0 though? Not very useful.
6. We are going to create a new GET route for our API:

   ```js
        app.get('/getnumber', function (req, res) {
           res.setHeader('Content-Type', 'application/json');
           res.send(JSON.stringify({ iserr: false, number: number }));
       })
   ```

7. Now that we've done that, Its time to make the number on the page change, So, When the page loads\( At the top of your code in the script tag. \) add in a request to get number, Parse the json you get back \( using JSON.parse\(\) \), And set the text on the page to the value of number!

\*Since the API is running on your own computer, You don't need to specify an ip address, Simply make the request to '/getnumber' .E.G.

```js
   fetch('/getnumber').then(...
```



