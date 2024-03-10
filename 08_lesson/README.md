# CSS Lists

## Ordered List

### list-style-type
```
ol {
    list-style-type: decimal;
}
```
decimal is the default value

list style type and all the properties we'll look at can apply to unordered lists as well

```
ol {
    list-style-type: disc;
}
```
we're just looking at this first with the ordered list so i'm going to go ahead and choose something here that will make this look like an unordered list at first so let's look at bullet i believe it was bullet let me check the selection and did i see bullet here not bullet it's disk there we go i call
2:20:02
it bullet points but they're actually disks is what they're referred to so this looks just like our unordered list now so the only way we could tell that this is an ordered list is to actually look at the html code at this point so we can make one look

## list attributes
***attributes we can add that will change how our list appears***

## list-style-type: none; 
``` 
ol {
    list-style-type: none;
    padding: 0;
}
```
that we could not have any kind of bullet or numeric out to the left so let's just put none here and save and you'll see that ***that's eliminated*** but notice ***it's still indented and that's because we have some default padding*** so we would have to set the ***padding to zero*** if we want our ***list items to go all the way back to the left***

## list-style-position 
## text-align
```
ul {
    text-align: center;
    list-style-position: inside;
}
```
list style position but first let's look at an issue that might get caused with list style position so in our unordered list if i set the text align to center and save notice what happens to the bullet points i've centered the text but the bullet points are still to the left some browsers have been known to handle this differently and send the bullet points to the middle and some leave them to the left and the difference is the list style position default value some browsers have a default of outside such as chrome and some have it inside or at least they have at one point i haven't checked browsers in a while instead of chrome but right now i have to set the list style position to inside to get the bullet points to align with the text but if we set them to the default outside they stay out to the left 

## Typography 
### color and line-height
```
ul {
    color: #00f; 
    line-height: 1.6;
}
```

if you set the color property it changes the bullet points and the text to blue we can set other text properties to or typography properties such as line height so i'm going to set this to 1.6 and you'll see some extra space between each of the list items 

## list-style-image 
```
ul {
    list-style-image: url("../images/checkmark.png");
}
```
list style image and we can set an image to use instead of the bullet points

## list-style
```
ul {
    list-style: square url("../images/checkmark.png") inside;
}
```
squares here for the bullet points but then we can also supply an image and when we do that the square becomes the fallback in case the image would not 
load and so now when i save we've once again got the image and then finally we can provide the position and so i'll say inside and now the images are over with the text of each list item so this is called shorthand we just say list style and we can provide one two or all three of these values that would be the list style type the list style image and the list style position 

## list items 

```
li {
    color: red;
}
```

```
ul li {
    color: red
}
```

we can also override styles from the unordered list for example on each list item now this would apply to all list items even in the ordered list because i'm just saying li and not specifying the unordered list or the ordered list as well but we can override styles because this comes later in the cascade as well but it's also more specific because we're down to the nested list items so if i wanted to change the color of all list items let's do something obvious here to red and there i put a hashtag first there we go just the word red now they've all changed to red however if i just wanted to change the unordered list items i'd have to put the ul first and then save and now it just applies to the unordered list items

## pseudo class
### :nth-child()

```
ul li:nth-child(2) {
    color: red;
}
```
- number 
- odd 
- even 

however what if i just wanted to make the second list item read now we can use another pseudo class i'll put a colon and then nth which is nth des child and then parentheses and now i'll just put the number 2 inside the parentheses and notice it only changed the second list item in the unordered list to red

so we were more specific and we just changed one list item likewise our nth child ***pseudo class also accepts the words odd*** so if we pass in odd now the odd numbered list items are red and likewise we could pass in ***even*** and do the same so now we're back to just number two because it's the only even number and it has turned red 

## Pseudo Element 
***Pseudo Element starts with two colon ::***

### ::marker
```
::marker {
    color: black;
}
```
we can ***change some things about the marker*** and that's usually what we would have here for a ***bullet or letters outside of an ordered list or numbers*** 

::marker keep color the color of text as it is 

```
ul ::marker {
    color: re;
    font-family: fantasy;
    font-size: 1em;
    content: "Only $5>>";
}
```
```
ul li ::marker {
    color: re;
    font-family: fantasy;
    font-size: 1em;
    content: "Only $5>>";
}
```
we could say just apply that to our unordered list and this is just like above where we supplied the ul

we could also actually say li here and it would be the same result as well but it's all markers in our unordered list so we don't have to put the li there and it identifies the unordered list and changes


we could add left padding but since these are positioned inside the left padding would be to the left of the markers so that wouldn't work 

creative with this content you can put in what is called an spg and those are often used for images and icons you could also put in something called font awesome icons and other types of icons as well so this does hold different types of content but it's easy just to type in here and show an example 

### attribute value 
```
<ol start="5" reversed>
    <li>Step One</li>
    <li value="26">Step Two</li>
    <li>Step Three</li>
</ol>
```
we can also specify a value so if we say value here and we put in 26 this will definitely make a difference now notice z is the 26th letter of the alphabet so the number corresponds still to whatever the order is and we're going in reverse order