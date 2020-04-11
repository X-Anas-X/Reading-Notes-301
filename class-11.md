# _EJS Embedded JavaScript templating:_
>- A simple templating language that lets you generate HTML markup with plain JavaScript. 
>> No religiousness about how to organize things. 
>>> No reinvention of iteration and control-flow. It's just plain JavaScript.

- intitle: Returns results where the text following this keyword is found in the title.
- inauthor: Returns results where the text following this keyword is found in the author.
* inpublisher: Returns results where the text following this keyword is found in the publisher.
+ subject: Returns results where the text following this keyword is listed in the category list of the volume.
- isbn: Returns results where the text following this keyword is the ISBN number.
- lccn: Returns results where the text following this keyword is the Library of Congress Control Number.
- oclc: Returns results where the text following this keyword is the Online Computer Library Center number.


Node Setup
{
    // server.js
// load the things we need
var express = require('express');
var app = express();

// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file

// index page 
app.get('/', function(req, res) {
    res.render('pages/index');
});

// about page 
app.get('/about', function(req, res) {
    res.render('pages/about');
});

app.listen(8080);
console.log('8080 is the magic port');
}
