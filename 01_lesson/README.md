# CSS Introduction

[CSS Documentation mdn](https://developer.mozilla.org/en-US/docs/Web/CSS)

[Anatomy of CSS mdn](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics)

## There are three different ways to apply css to our document 
- External Stylesheet
- Internal Stylesheet
- Inline with an element

### External Stylesheet
```
<link rel="stylesheet" href="css/style.css" type="text/css">
```
type="text/css" 

you may see some older code that has a type attribute here but mozilla now points out that this is no longer required and is actually kind of frowned upon so we do not want to include that but you may see older code with it it doesn't break the code if it's there it's just not the modern way of doing that 

```
<link rel="stylesheet" href="css/style.css">
```
This is the modern way the link external stylesheet

### Internal stylesheet
```
<style>
    color: limegreen;
</style>
```

### cascade
internal does it take precedence over the external
not really just it's interpreted as another style sheet either way now normally i use external style sheets but there is no difference as far as the browser is concerned what is the different is the cascade or the order 

### Inline CSS
```
<p style="color:blue">
```
i really don't need a semicolon because i don't have any other declaration here if i had more than one i'd have a semicolon in between 

blue over here this does take precedent over either type of style sheet internal or external because it's applied directly to the element itself 

inline css this is really not the way to do it though you really want to avoid inline css if you can


## note
but what we want is a separation of concerns so the best way the way that is commonly used is the external style sheet it keeps your css code completely separate from your html

## color and validator
[W3C CSS Validator](https://jigsaw.w3.org/css-validator/)

it's using the american spelling of color there could be other english words that are different but notice how visual studio code knows there's already a problem here and if i save this purple is not applied to our document

it's back to the default black text so we need to spell things with american english i guess is the best way to put it our dialect without the u in color and there could be some other words as well but notice we didn't get an error or anything if we do put in color the wrong way it's just ignored and that is something about css and sometimes it's hard to detect when you've done something wrong because you're not getting an error thrown like programming languages the rule or the declaration i should say not the entire

rule but this declaration is just being ignored because we didn't spell color in the way css expects so if i change that back once again we have purple text now one way we can detect problems in our css is to validate our css files 