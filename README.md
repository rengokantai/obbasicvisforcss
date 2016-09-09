## obbasicvisforcss
###Chapter 1. Basic Visual Formatting
####Basic Boxes
- Nonreplaced element  
This is an element whose content is contained within the document. For example, a paragraph (p) is a nonreplaced element because its textual content is found within the element itself.  
- Replaced element  
This is an element that serves as a placeholder for something else. (img)  
Most form elements are also replaced (e.g., <input type="radio">).  
- Block  
generate new lines before and after element  
- inline 
margin, padding and border can be set on inline-level elements, height and width will not.  
[explanation](http://stackoverflow.com/questions/5699967/displayinline-with-margin-padding-width-height)
- inline-block  
This is a box that is like a block box internally, but acts like an inline box externally. It acts similar to, but not quite the same as, a replaced element.  

####Altering Element Display
#####Changing Roles
An inline element can be a descendant of a block element, but the reverse is not true.  
(only a element premits,see below)
[Are block-level elements allowed inside inline-level elements in HTML5?](http://stackoverflow.com/questions/6061869/are-block-level-elements-allowed-inside-inline-level-elements-in-html5?noredirect=1&lq=1)  


#####Horizontal Formatting

#####Horizontal Properties
Seven properties: margin-left, border-left, padding-left, width, padding-right, border-right, and margin-right  
Of these seven properties, only three may be set to auto: the width of the element’s content and the left and right margins. The remaining properties must be set either to specific values or default to a width of zero.  

#####Using auto
```
div {width: 500px;}
p {margin-left: 100px; margin-right: 100px;width: 100px;} /* right margin forced to be 300px */
```
#####More Than One auto
```
div {width: 500px;}
p {margin-left: auto; margin-right: 100px;
    width: auto;} /* left margin evaluates to 0; width becomes 400px! */ 
```
#####Negative Margins

#####Percentages

#####Replaced Elements

#####Vertical Properties
Only three of these seven properties may be set to auto: the height of the element, and the top and bottom margins.  
If either margin-top or margin-bottom is set to auto for a block box in the normal flow, they both automatically evaluate to 0.  

#####Percentage Heights
However, in cases where the height of the containing block is not explicitly declared, percentage heights are reset to auto. If we changed the previous example so that the height of the div is auto, the paragraph will now be exactly as tall as the div itself:
```
<div style="height: auto;">
    <p style="height: 50%;">NOT half as tall; height reset to auto</p>
</div>
```
######Auto Heights
If an auto-height, normal-flow block box has only block-level children, then its default height will be the distance from the top of the topmost block-level child’s outer border edge to the bottom of the bottommost block-level child’s outer bottom border edge.  
Therefore, the margins of the child elements will “stick out” of the element that contains them.  
However, if the (parent)block-level element has either top or bottom padding, or top or bottom borders, then its height will be the distance from the top of the outer-top margin edge of its topmost child to the outer-bottom margin edge of its bottommost child:
[see fiddle](https://jsfiddle.net/rengokantai/vgrvtruu/)

#####Negative Margins and Collapsing



####Inline Elements
#####Line Layout
inline long text will collapse it line-height not set.
[see fiddle](https://jsfiddle.net/rengokantai/ft0vqqyp/)  
[css-tricks text with padding](https://css-tricks.com/multi-line-padded-text/)  
text-align (tbc)

#####Basic Terms and Concepts
- Padding, borders, and margins on nonreplaced elements have no vertical effect on inline elements or the boxes they generate; that is, they do not affect the height of an element’s inline box (and thus the line box that contains the element).
- Margins and borders on replaced elements do affect the height of the inline box for that element and, by implication, the height of the line box for the line that contains the element.  

#####Inline Formatting
It’s important to understand that line-height actually affects inline elements and other inline content, not block-level elements—at least, not directly.  
We can set a line-height value for a block-level element, but the value will have a visual impact only as it’s applied to inline content within that block-level element.  

Declaring (parent element)
```
p{line-height: 24pt;} 
```
means that the minimum heights for each line box(child element) is 24 points.  
Technically, content(child element) can inherit this line height only if an inline element does so.  


#####Vertical Alignment
