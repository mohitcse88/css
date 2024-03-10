# CSS Styling Links

***font family stack word use for font family value***

***styling our hypertext links is really an extension of the typography***

## Links or Anchor Tags

it's still text so a lot of the things we learn about typography we can apply to our links but also these links have
their own default styles that are different from the rest of the text on a page and when we talk about links in html we're talking about an anchor tag and usually that links to something with an href attribute 

### Default style of Links 
- default styles of these links they're underlined
- if the link has not been visited it's a blue color
- if the link has visited it's color is purple
- when we point at a link it changes our cursor from this arrow to a pointer it's a little hand pointing its finger at the link so that is called a pointer cursor
- when we click on a link so i'm going to click and hold down on this link and it turns red so this is when the link is active and that is another default style that is set

### a 
```
a {
    text-decoration: underline; 
    cursor: pointer;
    color: blue;
}
```
Above these are default style 

****cursors have semantic values*** and i'll see what visual studio code pulls up there's lots of different choices here but let's look for example at a not allowed cursor and it has a semantic value it tells us something just when we see it so when i point at javascript you can see we get the little icon that says this is not allowed but default style is ***pointer***


## Pseudo Class 

### :visited
```
a:visited {
    color: purple;
}
```
It is the default color of visited link 

visited pseudo class and pseudo classes represent the current state of the element because a state of an anchor element can change it is either been visited or it hasn't

### :hover
```
a:hover {
    color: dodgerblue;
}
```

when we hover over the link we have changed that state it's now in the hover state and it is changing the color of the link

### :active 
```
a:active {
    color: red;
}
```

### specificity

order will be:- 
- a
- a:visited
- a:hover
- a:active

if i just put in an anchor element you can see the score is just 0 0 1 but if i put in an anchor element with a visited or any other pseudo selector now the pseudo selector

here is a class i said pseudo selector a pseudo class i'm selecting the pseudo class classes attributes and pseudo classes so this has more specificity and that's why the visited link continues to stay purple even though the anchor element comes afterwards in the cascade but that's not usually the order we want things we usually kind of want to think about it in the order that we would have them so i'm going to put that visited back but now visited hover and active all have the same specificity and one can overwrite the other so we really have to think about the order we put those

in let me save this and right now they're all working because this is the proper order have your anchor tag and then have your visited pseudo class your hover pseudo class and finally you're active and they should all work so when we hover it works visited of course is working and if i click active it is working however if i rearrange these they may not so let me go ahead and take hover and put it above visited and so now visited comes after in the cascade and

when i hover that still works it hasn't been visited but let's check our visited link the hover doesn't work anymore so it's important to have these in the correct order i'll take hover and put it back where it belongs in this order so you want your anchor tag then your pseudo class of visited then your pseudo class of hover and finally your pseudo class of active 

## a:focus
```
a:hover, a:focus {
    color: dodgerblue;
}
```

focus pseudo class and this really makes your page more accessible because if a visitor or a user of your page is using a screen reader and instead of using a mouse they are tabbing through your page notice that right now we've selected the first link here and it has the outline around it i am tabbing through the links and by doing that when it has focus it is changing the color of the link just like we did with the hover and that's important to make your page accessible as well


## Opacity 
```
a:hover, a:focus{

    color: hsl(189, 44%, 49%, 0.8);
    /* opacity: 0.8; */
}
```
opacity property which is making something transparent and remember with colors we could add that right inside of this hsl as well but i'll show you how to do it here with the opacity property and let's put this to 1 would be the max and 0 would be completely invisible transparent

## a:focus

when we focus and i'm tabbing through we're kind of highlighting the links