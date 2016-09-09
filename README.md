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
