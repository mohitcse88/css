# CSS Colors

***140 colors available in html*** and visual code studio recognize all these names

so we also have to consider the contrast when we pick colors to make it legible and readable for our viewers and it also needs to be accessible and there are contrast ratios that are specified

## Background-color & Background
```
body{
    background-color: blue;
}
```
```
body {
    background: blue;
}
```
Above both code are same
***background*** is the sorthand of ***background-color***

## Color pallete in visual code stdio 
we chose those through visual studio code there the color palette just popped up

## Color
```
body {
    color: darkblue;
}
```
color property use for font 

## RGB  - Red, Green, Blue
```
body {
    color: rgb(255, 0, 0);
}
```
## override
color of text on the body but then we can override it inside of some of the elements so let's say our paragraphs here and we want to override that with a different color so maybe we want a blue text for the paragraphs 

## RGBA - alpha channel
a stands for alpha channel and that alpha channel guides the transparency it has value from 0 to 1.1
```
p {
    color: rgba(0, 0, 0, 1)
}
```
1 is just like the alpha channel wasn't there that's normal so that would be the full black color and it matches the headings that  we have on the page so you don't see a difference

```
p {
    color: rgba(0, 0, 0, 1)
}
```
but 0 would make it completely transparent and all of our paragraphs have now disappeared 

## hexadecimal value
```
p {
    color: #000000;
}
```
#RRGGBB

hexadecimal which is a common way to specify colors here the color palette keeps wanting to help me so we will be using that very soon hexadecimal also works like rgb and it has its own way of coding the values though it goes from 0 to 9 and then also uses letters a through f 

0 just like we learned with rgb is the absence of color

f is the highest value 

i was typing color names like dark blue and everything else here that starts with dark look at the hex codes over here to the right visual studio code is already helping show you all the different hexadecimal codes for these so we can of course get those codes by typing color names

- shorthand when the color codes match so two zeros two zeros and two zeros is black but it could be represented just by saying zero zero zero 

#000000 insetead of #000

- because each pair matched likewise two f's two f's and two f's is white so we could just say fff and 

each single f represents a pair 

#ffffff instead of #fff

#ff0000 instead of we could say #f00

- 80 80 80 doesn't have shorthand it's gray but the 8 0 isn't a pair so it's not a 0 0 or an 8 8 so you can't really do a shorthand for a hex code like this so
not all hex codes have shorthands just the ones that have pairs

## color pellete
- color plette at the left side
- tranparency between the color pelete and hue or alpha channel
- hue at the right side 
- bar at the top side

## Colors pellete picking tools
[coolors.co](https://www.coolors.co) - this is a color picking tools

by using space bar we can change or generate new colors

[colors.co contrast checker](https://coolors.co/contrast-checker/112a46-acc8e5)

[webaim contrast checker](https://webaim.org/resources/contrastchecker/) 

### legibility and accessibility are very important considerations as you pick colors for your web page