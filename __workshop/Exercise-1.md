# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything. 

Take the time to explain it to each other. 

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
// Answer here
create server
create an empty array
create input + submit elements
create element 'p' which includes the value of the input, sent on submit
on submit, .forEach the array which appends 'p' into the list div with appropriate styling

```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
// Answer here
body-parser is used to receive somehow the information from a POST form,
receiving data and taking it server side with the req.body
where is it related?
    - server.js line 24 
    - handlers.js line 7

```

## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
// Answer here
line 23 is calling a function (get statement) that has the code to render a page
line 24 is calling a function that declares variable item from the req.body created on form submission, pushes variable item to the items array, then refreshes the page.
```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here
line 6 is defining separate variables within separate .js file that defines the variables with the require function. require function takes the path of the handlers.
handlers.js must return with a module.exports of the item
```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
// Answer here
items is being used by the handleFormData to push inputs from the post form onto the page. then the handleFormData function refreshes the page.
the items are then on page load, with .forEach, create a li item and adds it to the ul todo-list (homepage.ejs line 7)
```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here
the page will populate the list based on the item array on page load. redirect to home page will refresh the page

``` 

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here
the extra functionality in the handle 404 takes the original url that the user inputted into the browser, in the path key with the value of original url, and prints it on the 404 page.

```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
// Answer here

homepage -
    1 header partial
    2 container div
    3 todoInput partial
        todoInput
        1 describes form type (post/get) and send to /form-data page
        2 labels item 'item' (not descriptive for code) TODO item
        3 describes the type of input, placeholder and most importantly turns the item into an object with the key of item and value of input
        4 submit
        5 end form
    4 //
    5 content wrapper
    6 create ul
    7 foreach on every item in the items array
    8 cont foreach - creates a li item for every todo-list--item
    9//
    10//
    11//
    footer partial
```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here
2 and 7 are variables being declared in the styling. in the homepage.scss they are being used to scale the input height and content width of elements without styling said elements

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here

to call a stated variable value in SCSS or SASS for any sort of numerical operation #{variable} must be wrapped!
like backticks of css
```







