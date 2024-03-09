# CSS Box Model

***we know our font size is impacting the default margin***

## CSS reset
```
* {
    margin: 0;
    padding: 0;
}
```
sometimes we just want to reset the browser settings for all the margins and all the padding and just take control of them ourselves and that's why we use a css reset and a very basic css restart starts with the wild
card at the top and then we set margin for all elements because remember this wild card selects all elements so we set the margin to zero and we set the padding to zero

## Box-Sizing: content-box;
```
* {
    box-sizing: content-box;
}
```
this is default is content-box and if we save we won't really notice a change here it didn't really change anything because that is the default so what the content box does is it says okay the size that we're setting is this for the content and the content only it doesn't include calculating the size of the padding or of the border or of the margin at all so instead of 50 percent i'm going to set an absolute width on here so we can compare and i'll set this to say 400 pixels and save now let's look over here in our box and we can see the content is 400 pixels but that doesn't account for the padding



## Box-sizing: border-box; 
### content-box vs border-box

```
* {
    box-sizing: content-box;
}
```
what we have here is not the 400 pixels we were expecting we took up more space than that but if we set this to border box instead of content box then we'll get what we expect and it's much easier to calculate so now notice our content over here is not 400 pixels is 348 and then we can add in 24 pixels of padding on each side and two pixels of border on each side and then we can get our total of 400.

so what borderbox does is it really helps us calculate the sizes that we are assigning because it goes ahead and includes the border and the padding it does not include the margin the margin is on the outside of our css boxes that we create whichever elements that we're styling so the margin is not included in that calculation however the rest is so the border and the padding and the content all add up to that 400 pixels

## margin 

```
margin: 3rem auto; 
```
auto keyword only work for left and right 

It doesn't work for top and bottom 

## Border: width style color;

### border-top-width
### border-top-style
### border-top-color


## outline: width style color; 

we're covering border one other setting to cover is outline outline is not part
1:31:59
of the box model because the difference between it and the border is that it doesn't take up space but you style outline much like you would the border so here i'm going to choose 5 pixels and i'll choose solid and then let's make the outline a different color entirely let's go with purple and if i save this now we can see purple wrapping outside of our border but again the outline is not calculated because it doesn't take up space so it's not calculated into that box model equation another property that the outline has that is very handy is outline dash offset so instead of being right up against our box we can say we want the offset to be 5 pixels and save and see how we pushed it now 5 pixels further out from our border so it's offset 5 pixels from the rest of our box and something worth considering sometimes is using a negative value so if i put in negative 10 pixels we'll now see the outside the outline is inside of our box here and so let's go ahead and change this some more so we
1:33:11
get it a little further inside maybe even 20 pixels and save and we can clearly see the outline is now inside of our box model


