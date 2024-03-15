# CSS Display

## Block Level Element 
***block level elements have a default 100 percent width and they stack on top of each other*** as we see here now they've also got some default margin as well which is why you see space between the paragraphs

when i say 100 percent width i mean of what is available to them it's not always 100 of the viewport

```
main {
    background-color: aqua;
    width: 50%;
}
```

hey do have a hundred percent width default setting but it's a width of what they are given so i say they have 100 width of what they are given it's not necessarily 100 of the page

we see they're taking up 100 percent of that main element with block level elements 
```
p {
    background-color: lightgray;
    margin: 100px 50px;
}
```
***we can also apply margin and padding and height or anything like that to all four sides***

## Block Level Element and Inline Element
***We can apply some css with block level element but when apply on inline element we can not see any changes***

## Inline Element 
margin and height 
```
.opposite {
    background-color: #333;
    color: whitesmoke;
    margin-top: 100px;
    height: 200px;
}
```
padding 
```
.opposite {
    background-color: #333;
    color: whitesmoke;
    padding: 1rem;
}
```

we can not see any change in span element which has class opposite we can't apply a top or bottom margin to a inline element likewise we'll try a different one let's go with height 200 pixels it doesn't change once again height cannot 
be applied and

***padding applies just a little differently*** so let's look at that and let's go with one rim and it looks like everything is as as expected here where we have a one rim padding top bottom left and right however

***if we go ahead and increase that let's say 4m look what happens it overlaps the above paragraph*** and ***we probably wouldn't want*** that so now let's ***apply the display property*** and we've talked about this being already as a default inline and then of course paragraphs default to block and many other elements as well like the main element we talked about however there is another option and 

### display: inline-block;
that is ***inline dash block and let's see what happens when we apply that to our opposite class now our padding is still applied but it's not overlapping the other paragraph*** so it is now respecting the top and the bottom likewise if we come back and apply that margin and let's just say margin dash top it could be bottom as well but we'll just put 100 pixels for the top and that worked as well now you can see we have extra space here and ***again this is applying just to that span element so not to the full paragraph itself*** and now

we could even add the height that we applied earlier that didn't work and we say 200 pixels and now our span element just got a lot taller so the inline block property ***value is kind of a hybrid here because we stayed inline in our paragraph this didn't create a new line like block would and at the same time it now allows some properties to be applied that normally wouldn't apply to the inline display*** 


```
p {
    background-color: lightgray;
}

.opposite {
    display: inline-block;
    background-color: #333;
    color: whitesmoke;
    margin-top: 100px;
    height: 200px;
    padding: 4rem;
}
```
so to quickly recap block level elements stack on top of each other and always create a new line inline elements do not stack on top of each other and do not create a new line block level elements automatically have a 100 percent width of whatever they are given if they're not inside of something that is limiting their width they will be the full width of the page inline level elements only take up the width of their content of course unless we put extra padding on them and then it has a little bit more width here because of that padding and then when we switch to inline block we get kind of a hybrid here where we can keep the content in line but we can go ahead and apply a top and bottom margin or a height and other things that typically only block level elements have so ***when would inline block be handy this could be handy***

if we were trying to turn a ***link into a button*** and sometimes people do style links as buttons and then you can of course have a row of those and likewise it could be something like turning a list into a row instead of a vertical list so it would be horizontal so let's look at an example of that 

## list
### default padding left
```
ul {
    padding-left: 0;
}
```
list have some default padding we can reset 

### margin-inline 
```
li {
    margin-inline: 0.5rem;
}
```
let's apply some margin between each one of them and what we can do here instead of saying top right bottom left as we typically would with the shorthand for margin we can just say margin inline and this will just apply to the left and the right so i'll say 0.5 rim

## CSS Reset
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
css reset but now you can see we are flush with the edges of the browser and our links

## display: none
list items are disapeared
```
li {
    display: none;
}
```
enitire bar are disapeared
```
ul {
    display: none;
}
```

value of none and look what happens all the list items just disappeared so let's go ahead and change that back so they show up and maybe we want our entire bar to disappear and right now that is an unordered list so let's say display and none up here and now it's entirely gone and that is exactly what happens it completely removes it from the document now we would still see it over here in our html but as far as the browser is concerned when it interprets the code the unordered list is not ***there now we rarely want to use this*** and that is because it removes it from that document flow and that means anyone using assistive technology screen reader would not be able to read anything 

***there are other ways to remove something from being visible from actually being viewed on the page*** but still have it in the document flow where accessibility might be still available and so we'll cover that in the future as well but right now just know that display none is a possibility






