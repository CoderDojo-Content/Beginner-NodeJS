1. In the Javascript tutorials you used an api, But now you are going to create one!
2. To make an api you are going to have to add a new _route_. Add this into your server file\( Just before the listen function \):

   ```js
    var number = 0;
    app.get('/addnumber', function (req, res) {
        console.log("Someone pressed a button!");
        number += 1;
        res.setHeader('Content-Type', 'application/json');
        res.send(JSON.stringify({ iserr: false }));
    })
   ```

3. So, What exactly did we do there?  
   1. First, We defined a new variable, Called number.  
   2. Then we said "When we get a _get request\*_" run this function.  
   3. We printed out that someone pressed a button and we added 1 to the number.  
   4. Finally, We sent back some JSON. Although sending back json wasn't really necessary in this case, IT is good practice to send back something to confirm that everything went well!

4. Restart your program and go to `127.0.0.1/addnumber` Hopefully your browser will show `{ iserr: false }` and your program will print out "Someone pressed a button!". Congratulations! Your first API is complete.

* Although we used a "get" request, There are many different types of request. The most common are POST and GET. Post is usually used for sending large amounts of data, And GET is usually used for retrieving large ammounts of data\( Although you can send a small amount with it. \).



