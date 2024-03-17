# Columns

## column-count

```
.columns {
    column-count: 4;
}
```
- convert the block level element row to the coulmn 

## column-width 
```
.columns {
    column-count: 4;
    coulmn-width: 250px;
}
```
- column width should essentially never be less than 250 pixels per column 

## columns
```
.columns {
    coloumns: 4 250px;
}
```
- This is the sorthand of cloumn-count and column-width

## column-rule 

```
.columns {
    coloumns: 4 250px;
    column-rule: 2px solid #333;
}
```
- this column rule is just like when we provide a border and the values go in the same order 

- now let's see what it does to our page and here we see 
the rules between each column now and of course they will disappear when the columns disappear if the sizing dictates that and so once we get down to one column even though we've said column rule should exist it won't if there's only one column but if there are columns to separate that's when the column rules start to show up and this will once again divide up to how many columns we've created so if we say a max of four columns we could have up to three column rules

## column-gap
```
.columns {
    columns: 4 250px;
    column-rule: 2px solid #333;
    column-gap: 3rem;
}
```
- column gap provide spacing between the column

## spacing problem 

```
.columns p {
    margin-top: 0;
}
```

- problem that exists right here i'll squeeze this over so we can see a little more and i want to pull this down so we can see some of the html above now as we get into our columns section and you can see it highlighted on the page as i highlight the elements here in devtools notice we have margin at the top and the bottom of each paragraph we didn't use a css reset so far so those margins have not been set to zero and that's okay we want spacing between the paragraphs but notice here in this first paragraph we also have spacing above the first

- paragraph so it's not setting flush with the top as the other columns are and then as we come down notice each paragraph is going to have its own top and bottom margin but there's one thing to consider here we need to remove that top margin from the first paragraph but let's see if we can just remove it from all of the paragraphs and what happens notice our margin spacing between the paragraphs as we see between the first and the second for example just is the spacing for that one margin essentially so here we see it again

- between the ***third and the second we just see that top spacing but if i highlight the second we just see the bottom spacing and they seem to overlap*** let's also discuss what's going on there so we'll go back to the code and i'm going to set another rule here and we want to say just our paragraphs that are inside the columns container so we'll say the columns class and then p let's say margin dash top and set that to zero and save now we go back to the browser and our first paragraph is flush at the

- top with the others but notice our ***spacing between the paragraphs did not change and that's a good thing it automatically happens in css and i don't believe i've discussed this before but that is margin collapsing so it's not going to double up the margin between the second and the third paragraph just based on having a bottom margin on say the first one and a top margin on the second one however now we've removed that top margin but the spacing remained the same*** 

- but ***previously it wasn't twice as much because of margin collapsing*** so that's a good thing and it's worth noting so we can actually just remove the top margin from each paragraph and not change the spacing of the others but it does fix the top alignment here making it flush with the other columns as we want it 

## Element Spliting
```
.columns h2 {
    margin-top: 0;
    background-color: #333;
    color: fff;
    padding: 4rem; 
}
```
- let's set the margin top to zero just like we did for the paragraph so there's not an issue there 

- let's see what happens as we resize that looks a little weird we have ***part of the padding at the top of the second column and the rest of the header here at the bottom of the first column*** that's kind of strange we might not want that let's get some more room and drag it over and see if anything else weird happens well not with the room we have but as this resizing occurs strange things could happen but we can prevent some of those strange things by ***applying another property inside of our h2*** 

### break-inside 
```
.columns h2 {
    break-inside: avoid;
}
```
- This is avoiding the splitting of the element but here header 

- now as we get to our two columns we notice it's on the second column which may not be the best thing that we want we might want that at the top of the second column but ***it's not splitting the header into two different pieces*** with part of it at the top and then part of it to the right and once we get down to one column it's just the one headerthere 

### break-before
```
.columns h2 {
    break-before: column;
}
```
- break dash before and we'll set this to column and there's good and bad with this so let's look at this overall so now notice we're at the top of the second column and that's fine and as we scroll and we have two columns now we're at the top of the second column again which is what we want instead of being at the bottom of the second column as we were before the problem comes when 

- ***we want to size down to one column notice what happens instead everything shrinks and we got three columns*** and that's not maybe what you would expect but this ***break before actually forces a column break so it forces there to be more than one column and the browser is trying to fit all of that in which is why it shrinks so probably not a great idea to use this break before column property if you know you're going to be shrinking your page down to that one column however the break inside with the avoid will keep your header that you might create or something else from being split between the two columns*** 

## column-span 
```
.quote {
    font-size: 3rem;
    text-align: center;
    color: #333;
    column-span: all;
}
```

- web page and we see our ***big quote and it's spanning all three of the columns*** and this is kind of like you might see in a magazine as well where they highlight a quote as you're reading the article 

- but something doesn't look quite right does it we've got all this space underneath but no space on top that's because this is a paragraph that's inside of our section container and remember we set the margin top to zero for all of those so let's go back to our code and now that we're inside of this quote class let's set the margin dash top to to rem and go back and take a look and i think you'll be surprised at what we see there's absolutely no change so what's going on well let's once again look at our code and see the problem what we have here is columns the class

## specificity 

```
.columns p{
    margin-top: 0;
}
```
- This is more specific
- columns which gives it a score of 10 as a class and then p as an element so it's got a score of 11.

```
.quote {
    margin-top: 3rem;
}
```
- This is less specific 
- ***columns p where we set the margin top to zero that is more specific than just having a class***
- quote we only have a score of 10. 

### Cascade
- so even though quote comes after this column's p definition in the cascade it's not as specific so that margin is not applying  
- what we could do is say dot columns dot quote and then notice we have a score of 20 
```
.columns .quote{
    margin-top: 3rem;
}
```
- It is work as expected.

## white-space
```
.nowrap {
    white-space: nowrap;
}
```
- browser and we resize our quote should not break the dude our author should always stay on the same line including that long dash and that's exactly what happened it all went down to the second line at the same time so we're no longer breaking the dude with his long dash into separate lines and that's the way we want to style
