# CSS Selectors

[CSS Specificity Calculator](https://specificity.keegan.st/)
## Element Selectors
```
body{
    font-size: 22px;
}
```
All of text on our page larger this is due to inheritance so these other element actually inherited from the body element and we'll get more into inheritance in just a little bit too

But this in itself is an element selector 

element selectors select all of the elements of that type so just specifying p for the paragraph element selects all paragraph elements 

## Class Selectors
you can choose the name of the class but make sure it makes sense and remember ***your writing code for others to read not just yourself***

***Classes can be used more than onces*** and they can be reused more than one element

***Classes are more specific than selecting all elements or paragraph***.

Classes are most common type of selector with css ***But more specific selector yet is an id selector***.

class is attribute in html 

## Id Selectors 
***Id should only exist once in an html document or they should be unique in other words***

***It is not good practice to really use ids inside of your css*** now it will validate your code has no problem using an id however ***typically you should classes and sometimes elements slectors***. But rarely if ever should we use an id selectors inside of your css.  they or ***Id do have other valid uses in form input linking to label elements***. and Javascript have some other uses of id attributes. But we try keep out them of css.

Id is a attribute in html 

## Group Selectors
```
h1, h2{
    color:blue;
}
```
if i remove the comma and save this declaration or our full rule set especially if we had more declarations none of it would apply to the h1 or the h2 

```
h1 h2{
    color:blue;
}
```
now what's going on here this selector is looking for any h2s that exist inside of an h1 it's not looking for an h1 or an h2 it's only looking for h2s that exist or are nested if you will inside of an h1 so that's why that didn't work that may be useful to know in the future but what we need is a comma in between and then we can select both the h1 and all h2s on the page with this rule set

## Nesting Selectors
```
p span{
    text-transform: uppercase;
    background-color: gold;
}
```
however this doesn't make a lot of sense ***p span***, this is a much better example  of where we should use a ***class*** we might name our class something like  ***highlight***

```
.highlight{
    text-transform: uppercase;
    background-color: gold;
}
```

inside of the index so we've come in here and find our span and i'll select both of these and then we can add the ***class highlight and that makes it reusable***

and now it's once again applied but this would keep our css much more organized and actually more reusable it's more flexible this way because we might have some ***span elements doing other things that we didn't want to apply this rule set too***

## Universal Selectors *
```
* {
    font-family: monospace;
}
```

universal selector and this means it's selecting everything on the page you typically only see this for what is called a css reset that we will cover in the future but just so you know it exists this selects everything so let's think about what we could apply here that would be applicable to everything so let's change the font and we'll set it to this mono space font 
and save and now you can see all of the text on the page turned into this monospace font instead of the default font that we had now this is not how we would use this again in the future we'll learn about a css reset that would use that selector but typically that's the only time you see that universal selector used

## Cascade
```
p {
    color: purple;
}
p {
    color: red;
}
```
the cascade css is an acronym for cascading style sheets and essentially that means css works like a waterfall it works from the top down and that means if i were to put in another definition i'll just copy this down for paragraph and where we have the color purple on our first paragraph it really applies to all but then of course the gray class overrides that on the final two but if i came here and said red instead of purple notice how this paragraph turns red and that's because it read this rule set last so first css
looked at this at the top it starts at the top and it works its way down and so it read this last essentially this is the last rule and that means whichever definition it reads at the last will be applied

now specificity can override this and that's where we talked about elements and then classes classes are more specific for example than just an element selector so we have our class here that has the color gray and it is overriding the red now if we remove this class and we save now they're all red but even though

color purple is crossed out and then color red is crossed out so
***css knows these rule sets exist for paragraph but it also knows it should follow what is the most specific using the rules of specificity***

***inspect, select a element and look the styles***
how it is being read by css in the browser or how the browser is reading your css and then see how those rule sets are being applied which ones are being overridden and which ones are actually being applied

## Inheritance
inheritance that is where another element inherits the settings from or the properties from its parent element

so the body element is parent to every other element here and so when we set the font size all of these other elements inherited that font size now

typically anything related to font or typography is inherited and that can include things like color line height alignment all sorts of settings dealing with the font and the typography however any properties that are not related to those things are not inherited

```
body {
    font-size: 22px;
    border: 3px solid black;
}
```

and i know that'll just take a little bit of getting used to as you learn more about css so for example this font size was inherited but another setting we could put is a border and i'll put three pixels so it's easy to see solid black and i'll save this now notice the border only went around the body element it didn't apply to all the other elements inside of the body so that's an example of something that is not inherited


### * universal selector 
```
* {
    font-family: monospace;
    border: 3px solid red;
}
```
universal selector let me go back to that and show you that this is not inheritance this is actually selecting all elements so here if i said a border and i'll put one pixel solid red and save notice it does apply to all elements that's because we selected all

the elements here so setting something here with the universal selector is not going to cause inheritance really because it's actually selecting all the elements itself

## Inheritance Importance
inheritance overall this can be very handy because it keeps us from writing repeated code in other words it keeps our code dry which is an acronym that stands for don't repeat yourself so we want to write less code and be more efficient and inheritance helps us do that

now some things are not inherited like i mentioned the border would be one of those 

```
button, input, textarea, select{
    font: inherit;
}
```
also form elements do not inherit say the font size and other typography settings so it wouldn't be that unusual to see something like this that would take a button and let's say an input a text area and let me see if i'm leaving anything else out maybe a select anything like that and we might see then font and set it to inherit and that would go ahead and make those elements inherit the font settings because just a mental note that form elements do not typically inherit those font settings

```
html {
    font-size: 22px;
}

body{

}
```
but now to take advantage of inheritance and write dry code we can use the body element which appears only once per page or we could use the html element and either would work oftentimes if you're just starting out and just remembering it might be best to just use the body oftentimes i use the html element because once again the inheritance applies there so we can save here without see the difference now i'll go ahead and apply it in html and once again we have the larger font because there

are for me at least some specific settings for the body and i like to see those separate so i often put all of my font settings in the html selector but again either would work

```
main {
    font-family: monospace;
}
```

one other element selector that i do use at times is the main element it is a semantic element and it should appear only once per page but then you have to be aware that you're only selecting the things inside of the main element so if we look at our page i've got the h1 inside of a header element and not inside of the main element so if i were to change
31:15
the font family inside of our main selector and i changed this to mono space which is easy to see the change with go ahead and save you can see all of the articles switched to mono space but our h1 heading is still using the other font 

## Important Flag
```
p {
    color: purple!important;
}
```
sometimes something's not working out and you're wanting to figure out why it's not working out or you just can't figure it out and you get frustrated i'm going to show you something that will work but i'm going to recommend that you do not use it it's kind of the nuclear option if you will and it's to put an exclamation mark and put important now see how red should be applied to this first paragraph but with the important flag right here after our purple setting and now i save notice what happened it turned the first paragraph purple 
notice what else happened it also turned the second paragraph and the third paragraph purple

now why is that well this important es
sentially ruins everything else it overrides everything

so really when you see it in code it's kind of an indication that it's not well organized or it's sloppy there's only a few reasons you would really want to use this and i feel i mean i'm hesitant to even show it because i feel like beginners could abuse this however you'll see it somewhere i just want you
to know it exists don't use it don't use it you need to learn how to organize your code and apply it correctly and only after you've learned css well enough to understand when to use that important flag that's the only time you should use it you should really not give up the struggle you will learn more by struggling and learning how to apply these selectors in the proper way without using that important 

## Specificity Calculator 
you can compare two selectors to see why they are working and why they aren't working or why one overrules the other 