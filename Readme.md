# CSS

    -> Simple Selector
        -> Element Selector
        -> Class Selector
        -> ID Selector
    -> Pseudo-class Selector
    -> Multiple Selector

## Element Selector

    style applied on elements by directyly using the tag name ex
    paragraph <p>, body <body>, header <header>, footer <footer> , <h1>, <h6> etc  .

    we can style them by justing using there name like this
    p{
        property-name : value;
    }
    h1{
        property-name: value ;
    }

## Class Selector

    class selector is used to group the element tag to apply common style
    for that in element tag we have to write class="name".
    and to style that element using that class name we can use dot ( . )
    ex :
    .name{
        property-name : value;
    }

    note : class is used to group element together to apply common style , so one class can be applied to many .

## ID Selector

    Id selector is used to set uniquness for an element . and can be write on element as id="unique-name"
    to style id based element we can use # (hash)
    ex
    #unique-name{
        property-name : value;
    }

## Pseudo-class Selector

    A pseudo-class is akeyword added to a selector that specifies a special state of the selected element.
    a state example can be when we hover over the element

    <p class="hoverME">hi</p>

    in css we can write a pseudo-class on hoverME class by using a : (colon)

    ex
    hoverME:hover{
        color:blue;
    }

    this will change the color from default to blue when we will hover and reback to default when cursor leave

## Multiple selector

    grouping many selector to apply the css style to all in one go . by using comma we can do this
    for example
    p,h1,h2{
        color:red;
    }

## Universal Selector

    *{

    }
    thers more read mdn

## Nested Selector

    -> descendant Selector ( seperated by a space while write slector name in css for one level child )
    ex h1 h2 {
        color : red;
    }
    this can be grouped by comma for other descendant
    -> Child Selector
    For the cases where you only want to target direct children (nested only one level under)

    use > greater than symbole .
    ex h1 > h2{
        color: red
    }

    read more why 3 level nesting not working i have doubt about this

    -> Adjacent Sibling Selector
        to apply style on siblings
        use add symbol
        ex two siblings h1  and p .

        h1+p {
            color:red;
        }
     -> General sibling Selector
      instead of just one sibling , selscting all by using tilde ~
      h1 ~ p{
        color: red;
      }

## Attribute Selector

    -> The CSS attribute selector matches elements based on the presence or value of a given attribute.
    <div lang="en-us en-gb en-au en-nz">Hello World!</div>

    div[lang] {
        font-weight: bold;
    }

    this one is cool , read more in mdn

# add styling in HTML

-> Inline
write in element tag <p style="font :red">hi</p>
-> INternal
write css in style tag inside head in html
-> External
write css in an external file.css and add it in head of html by using link

    <link rel="stylesheet" href="file.css" />
        rel is here saying relationship between current html file and the external file i am refrensing to

priority : inline> internal>external

# Specificity

if we add multiple rule to the same leemnt then it will be hard to guess which one gonna overwrite
so for this Specificity rules comes handy

    !importand > inline css > ID > Class > tag selector

# Box Model IN CSS

according to box model concpet every element on a page
is a rectangle box and may have width , height , padding,
borders and margins .

content in the main part of the box and height , width
are said to be measurment of inner content .

on the top of content there is padding , on the top of padding there is border ,on the top of border there is margin

#
