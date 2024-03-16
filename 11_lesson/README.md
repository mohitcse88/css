# Floats
div and all of our paragraphs are block elements and so they stack on top of each other but when we float this div element that we've created here it will take it out of the normal flow of the page and we should see our text wrap around this and you could picture this as being an image if you want to but whatever content we would float and we can float it left or right the text will wrap

## Float: left;
this is applied on div
```
.block {
    width: 30vw;
    height: 30vh;
    background-color: #000;
    color: #fff;
    padding: 1rem;
}
.left {
    float: left;
}
```

This is applied on paragraph
```
p {
    margin-left: 10px;
}
```
we can see the text has wrapped up around the div so now it's more like you're used to seeing in a ***newspaper where you would have an image or something over to the left or the right and the text*** would go around it 

margin left for the paragraph and say i applied 10 pixels look what happens it still is flush here you see it moved 10 pixels over here this float is not inside the normal flow so the margin is applied from the left over here and not where we would expect it to be at the left edge of our text and we can see that even more so if i do something greater like say 20 percent and now yes it moved this way over but it didn't move the text here at all so we can't really apply that correctly by applying it to the paragraph instead we can apply some to the actual block

itself so let's do that and we can say well let's do it to the left because we might do it differently for the right so let's do it to our left class here so we would have a margin on the right side of let's say one rim so we should be able to see that and now that makes the difference that we wanted right here and also it makes our text once again flush with what would be our image or our div that

## Some Instances
there could become some instances where we want to handle this a little differently maybe we want to wrap this first paragraph and this div that i've floated to the left in a container and kind of highlight that at the top and then have the second paragraph start afterwards we might have to handle that differently or let's say we didn't even have the container but we didn't want this second paragraph to wrap and in the past it was handled a little differently than it currently is so

### clear: both; 
```
.clear {
    clear: both;
}
```
let's create one more class and i'll show you something you may see once again i would say in more legacy code

we want to wrap this first paragraph and this div that i've floated to the left in a container and kind of highlight that at the top and then have the second paragraph start afterwards we might have to handle that differently or let's say we didn't even have the container but we didn't want this second paragraph to wrap and in the past it was handled a little differently than it currently is so let's create one more class and i'll show you something you may see once again i would say in more legacy code

let's call this a ***clear class*** and then inside of this class we'll say ***clear and we can say just right or just left if you want to clear something that is specifically floated left or right but it's very easy to just say both*** and then it will clear both and you'll see what this does in just a moment here so what i need to do is come back and then after the first paragraph if i wanted to clear that the old way would be to apply another div to the page and give it this class of clear and just leave it empty and we would save 

and then you can see the second paragraph doesn't start until after this div so it is cleared and that allows us to go ahead and start the second paragraph after both of these

## Flow of Page

***but this could still be a problem if we had this in a container*** and i will show an example of that so let's apply a container to the div and the first paragraph and i'll just make it a section element and wrap it around those so i'll cut that closing tag and put it here after the first paragraph and save well i want the formatting it didn't do it for me 

tab that in and save and then we can style our section to make it a little more obvious what's going on i think i'll scroll up just a little bit more there we go and so now we have a section and inside the section i'll say background color and we'll give this a color of bisque which is kind of a neat color and after bisque let's go ahead and apply a border so we'll say border one pixel solid give it a flat black color and a little bit of padding one rim okay and let's save and see what we get

well this looks okay right now i don't see a problem but what if we removed this div with the class of clear and save well still no problem let me shorten up this paragraph by several words and then see what we get and now when i save i just had too long of a paragraph to actually highlight the problem before but now when i say we can see the problem this float is once again not in the 

***normal flow of the page so the container is only expanding based on the text content and when i had more text content it looked okay but you can
really highlight the problem if you don't have enough text content to push the container down***

so we can definitely see a problem that needs to be rectified and that is because we don't want the container to just go halfway we want it to go ahead and contain the full item the full element that we have floated left or right so we think why not go ahead and ***put that div back in place that had clear well let's try that and see what happens i've got the clear div there now and you can see it clears the paragraph but it doesn't help the container***

so let's once again remove that div i'll just press ctrl z to undo those changes and control s to save so now the paragraph is coming back up and i will show ***two different ways to fix this***

### overflow: auot;
```
section {
    overflow: auto;
}
```
- one past approach that you may see in code is to set the overflow to auto but this is in more legacy code once again but notice it does work so i wanted to show that overflow auto is a ***possibility*** to go ahead and get the container element to extend all the way down and contain the full element that is floated either left or right 

### display: flow-root;
```
section {
    display: flow-root;
}
```
however the ***correct current way as noted by mdn*** is to say display and then say flow dash root and if we save that we once again have fixed the problem so if i remove that save we have the problem i'll put the display flow root back in and the problem is fixed so this is considered the ***current modern way to fix this problem*** 

in the past floats were also used to create columns on a page but that was because there was no other method available and now with modern css we do have other methods available including display flex and display grid that i will be covering very soon in future modules 

## Summary 

but right now just remember floats are used to float things to the ***left and the right really any element that you want to and you can wrap text around it and then you can also use floats inside of a container if you want to but remember to apply display flow root to the container*** so the container contains the full floated element and ***doesn't shrink based on the text content alone***