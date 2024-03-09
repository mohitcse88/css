# CSS Typography 

[Text Property Mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Text)

***Typography is the way that text arranged and presented***

## rem 
***rem means root em***

## Inheritance 
```
body {
    font-size: 2rem;
}
```
through inheritance font and text settings are usually inherited so the children of this body element would inherit the font size of 2rem unless we set a specific one on those child elements

## Form 
```
input, label{
    font: inherit;
}
```

however they do not inherit the size here inside of a form so notice the ***label has that font size inherited*** but it did not get inherited in the ***input or the button*** so after the body here we could also select both the input and the button and then inside of this we could say font and inherit and now they will both inherit that font size that we put on everything else


## text vs font 
when i'm speaking sometimes i will say font when i mean text but they are really two different things notice we have some text settings that aren't impacted by the font choice at all 

## text-decoration: none ;
```
p {
    text-decoration: none; 
}
```

and let's go over those first so let's select our paragraph here on the page and we'll set some text settings for that and the first one we should go over is text dash decoration and we can see the different choices we get right away when we choose text decoration because

vs code wants to help us one typical text declaration to set would be underline so let's go ahead and save this and now we can see our full paragraph text is underline another choice which is just the opposite is line and when we set that you can see now we have a line above the text instead of below it and then there's also line dash through and if we save that it does exactly what you expect it to it puts a line through the text maybe you just have a few words you want to cross out and you surround those words in a

span element and then you set this line through property for that specific span element and that would probably be a class you would create to do that so after we've gone over those text declaration settings the other one you may see is none now that is the default for a paragraph text like this but what if you had a link text links are usually underlined by default and so setting none would remove the underline on a link and those are the typical settings i'm not going to go over every setting today because

## text-transform: capatilize ;
```
p {
    text-transform: capatilize;
}
```

text transform and after that you can see our selections pop up here in visual studio code again so if we choose capitalize and save now it capitalized the first letter of every word in our paragraph likewise we could choose lowercase and now every letter is lowercase not just the first letter but every letter and then we could choose uppercase and we'll get the opposite as well and now we have all upper case

## text-align: justify;
``` 
p {
    text-align: justify;
}
```
- center 
- left is default and only left side uniform 
- right it make only right side uniform
- justify it make left and right side uniform

text align what we normally have is a line left so this is typically the default for paragraphs and you see this and look to the right this is not uniform over here each line has kind of a different ending point and this is how we typically see a paragraph when we're looking at a paper or something like that like a a school paper however a newspaper might choose to justify or a magazine paragraphs and now notice the right hand column is uniform here where it all ends at the same place just like the left side does and then of course we can text align right which is the opposite of text align left and now it's uniform on the right but it is not on the left 

## text-indent: 2rem;
```
p {
    text-indent: 2rem;
}
```
sometimes when we write a paragraph we want to indent that first line so let's remove this and save so you can see the default settings so here's our paragraph we have no indent up here at all but we can choose text dash indent and here is a good spot to use em units so i'll say 2em and save and now we have an indent of two m's that's em units and it just indents that first line of course we can set it to a bigger number and you can see it go over even further so you can really see it go into action however two seems about right here so if we need to indent that first line we can do that with text indent

## text property 
and of course there are more text settings that you can pull up as well and refer to mdn the mozilla developer network where they have great documentation for all of these another way to find out about text properties besides mdn is to just type text and then you can see visual studio code start to make suggestions here for some other settings 

## typograpy 
few other properties that impact typography that do not start with text or font so let's quickly go over those 

## line-height: 1.2;
```
p {
    line-height: 1.2;
}
```
line height line height accepts units just like we went over in our unit and sizes tutorial so we could use different percentages and things like that however it also
just accepts a number and the default is usually right around 1.2 so we probably won't see much of a change to our paragraph when i set the line height to 1.2 however it starts to look much better around 1.4 or 1.5 so i'll go with 1.5 and i think ***that really increases the readability of our paragraph*** 

## latter-spacing: 0.1em;
```
p {
    latter-spacing: 0.1em;
}
```

letter dash spacing and this does exactly what you'd think it would do it increases the space between the letters of the words so if we put in oh let's go with 1 m and save it really spaces those letters out 
doesn't it we probably don't want to stick with that unless we're going for some kind of special effect maybe down to 0.25 well it's definitely more readable but it looks kind of weird to me still maybe 0.1 and you may see text like that somewhere some time in a heading or something to draw attention to that looks like it may work but i wouldn't use letter spacing too often because it seems normal to me when it's just at the normal setting presented by the browser 

## word-spacing: 
```
p {
    word-spacing: 0.5em; 
}
```
word spacing so let's go with 2m there and notice the difference it really spaced those words out so we could come back maybe 0.5 and yes we've got some extra space between the words once again it's an effect more to me than it does anything to really increase the readability however maybe if we got to a much smaller size maybe it would help let's see well it's noticeable still i don't know if i like it better but it is an option 

## font-weight: 400;
```
p {
    font-weight: 400;
}
```
font weight that's essentially whether it's bold or not in normal or the ***default is right around 400*** so if i save this we won't notice much of a change well i noticed a bit of a change let's see what 300 is like and yet maybe normal was more like 300 for this particular font but overall for 300 to 400 is kind of normal let's go back and see what visual studio code offers for values that we could choose from so now you see we've got 100 through 900 900 being very bold and 100 being not bold at all and then there's also just some words we could choose bold bolder lighter and then of course normal so let's go with normal and see what that looks like well normal looks more like what we had at 400 there let's go with lighter and save and it's not too light but it's noticeably lighter than it was let's go with bolder and that's very bold we can definitely see the difference there so 100 would be very light and 900 would be very bold and if you don't set the font weight you can expect it to be somewhere right around what normal was to begin with

## font-style: italic; 
```
p {
    font-style: italic;
}
```
font dash style and if we set font style we're setting possibly the italic setting and if we save that's exactly what you expect we have italic text there is also oblique which essentially is a stronger italic it just has a little bit more emphasis there and as you might expect after learning about font weight it also has a normal setting so that is the default and it's basically that without setting a font style as well okay 

## Big Settings
### font-family: serif; 
```
body {
    font-family: serif;
}
```

now we get to the big settings something we typically set not on an individual paragraph unless we want to change the font specifically for the paragraph but let's set this on the overall body of the page this is the font family property notice visual studio code is providing lots of suggestions here that we'll go over in just a minute but there are some main generic families and one is ***serif and if i save it's pretty much what the browser default*** already was and this is the type of font family that we see in academic papers newspapers papers you'd see in school overall however on the web it's much more popular to use the sans serif family if i save that you can definitely see the change here and this text is more like you would see on many popular web pages even though there may be variations of then another generic family is mono space oops i didn't spell that right i need mono space there we go if i save that you can see mono space has the same spacing for every character so this looks much more like an old typewriter or something like that where it gives each character equal spacing then there is also the cursive family

popular to use the sans serif family if i save that you can definitely see the change here and this text is more like you would see on many popular web pages even though there may be variations of then another generic family is mono space oops i didn't spell that right i need mono space there we go if i save that you can see mono space has the same spacing for every character so this looks much more like an old typewriter or something like that where it gives each character equal spacing then there is also the cursive family

and that looks a little different as well you may have seen fonts like that before and i believe there's the fantasy family save that yes and that also looks different here i would possibly think about using just a little bit of letter spacing it looks a little crowded to me but overall those are the generic families but those are usually used as a fallback because we have more specific fonts that make some changes so when visual studio code was suggesting these font family values let's go with this first one we see here

courier new and then courier and i'm going to press alt z so the code wraps over here on the left so you can see this full font family setting so courier new is the first choice and then the second choice is a ***fallback so if our computer whether it's windows mac or whatever and they do have different fonts installed if our computer doesn't have courier new then it's going to look for courier and finally after that it's going to look for mono space so it doesn't necessarily use all three it uses*** the 

first choice if available if not it uses the second choice and if not the third also notice the courier new has a space in it and anytime the font name has a space in it you need to put quotes around the name to handle that spacing the names that don't have a space do not need any quotes at all so let's save this and here we are using courier new i believe on the page which looks a little different now let's choose something else from a ***different font family so we had the monospace family*** right there let's go


with ariel and you can see visual studio code instantly suggests a full font stack which is what these are when you have multiple choices this suggests ariel then helvetica and then finally the sans serif generic family so let's save that and this is a font you see much more often on the web overall and arial is fairly commonly installed on both mac and windows and probably linux any other type of computer okay after that maybe verdania is another one in that sans-serif family you would see and here this font stack has four choices


actually for dania geneva tahoma and then eventually sans serif also notice that sans serif does not need quotes around it because it has a dash it does not have any spaces so if we save that this looks just a little bit different than when we had arial now if we did want to choose a serif font instead of a sans serif font a very popular one is times new roman and you can see the suggestions here from vs code we've got times new roman in quotes again then times and then serif so if we save that this is more like what the default 


browser font looked like and i've got a couple of good links about what are called 

### web safe fonts
and that's essentially what is being suggested here by visual studio code when you use these stacks they're fairly web safe they don't need to be installed from an external source typically the computers would already have these available to the browser i'm going to switch this back to arial choose that 

## Google Fonts
[Google Fonts](https://fonts.google.com/)

choose an external font from google fonts and this is very common practice and we can load this in and then use it on our page so here's a very popular font roboto so we can select it and it says it has 12 different styles so now it takes us to the ribato page and you can see the different styles notice this says thin 100 here for this style now this means that that font weight is 100 essentially here's

light 300 light 300 italic so you can choose some of the styling right here at google fonts i typically choose not to and just get a generic font and then try to apply my own styles as well but you can see the different ways the font will appear and that's really nice to look at like that so i would typically just choose the regular 400 and see if i could modify it with my own css now there are different ways we can link to this google fonts lets us choose a link that we can put in the head element of our


html or it lets us choose an import let's look at the link version first so if i were to do that i would be choosing this link section here and it says i have more than one link selected so i previously had selected another font here i'm going to click the minus symbol remove it so i only have roboto and now there is still this link section i would need to copy all of this and then i would do that with control c for example now i would need to go back to my code so let's do that and here inside of the code i'm going to

need to go to the html and then let's make this take up the full screen for a little bit and inside of the html in the head section ***before the link to my style sheet because it needs to use the fonts i need to paste in these extra link elements that google provided so it's going to get the information from google fonts loaded in and then my style sheet can read it*** but although we're loading it in here we're not quite finished because we haven't applied it to our css so they will not be used yet at this point i'll drag this


back over and now google is also saying we need to apply this line in our css to use it notice roboto has a sans-serif fallback so it's part of that font family i'll copy that go to the css and where i had ariel helvetica and sans serif here i will replace it with what google suggested and provide roboto and sans serif now note they put ***quotes around roboto and that won't hurt anything either*** so we'll leave it as they suggest now let's go back to our document and notice we're using the google font


roboto now now ***you can choose more than one font from google as well the more you attempt to load in from google though the longer your page will take to load***

***so i suggest grabbing no more than you absolutely*** think is necessary i do want to show you how to use the import in your css instead of the link in your html so let's click the at import here and now you can see it's not quite as much code and what else i like about this is it goes right in your css if you want to notice they put it between the style element which 

could still go inside of the head of your html if you were to copy all of this i'm not going to select the style element tag the opening or closing just what's in between because i'm going to put this directly into my css file so now that i've copied the at import statement i would normally put it right up here at the top of my css and you want it before it would load anything in now of course this is wrapping the code because it's a longer line with the url but i'm going to save this i'm going to

go back to the html i'm going to remove all of those links that we had of course leave our own style sheet and now we'll still be able to use the roboto font even though i've removed those links from the head section of the html i now have the import statement at the top of my css and if i go back to our document i can even reload and we still have the roboto font ready to use because we've imported it at the top of the css 