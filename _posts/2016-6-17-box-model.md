---
layout: post
title: BOX MODEL
---
**How Are Elements Displayed?** <br/>
-There are quite a few values for the display property, but the most common are block, inline, inline-block, and none.<br/>
-We can change an element’s display property value by selecting that element with the Opening the Box Model CSS and declaring a new display property value.<br/>
-A value of block will make that element a block-level element.<br/>
-A value of inline will make that element an inline-level element.<br/>
-Things get interesting with the inline-block value. Using this value will allow an element to behave as a block-level element, accepting all box model properties.However, the element will be displayed in line with other elements, and it will not begin on a new line by default.<br/>

**What Is the Box Model?** <br/>
-Every element on a page is a rectangular box and may have width, height, padding, borders, and margins.<br/>
-Every element is a rectangular box, and there are several properties that determine the size of that box.<br/>
-The core of the box is defined by the width and height of an element, which may be determined by the display property, by the contents of the element, or by specified width and height properties. padding and then border expand the dimensions of the box outward from the element’s width and height. Lastly, any margin will follow the border.<br/>

**Width & Height** <br/>
-Every element has default width and height.That width and height may be 0 pixels, but browsers, by default, will render every element with size. Depending on how an element is displayed, the default width and height may be adequate. If an element is key to the layout of a page, it may require specified width and height property values. In this case, the property values for non-inline elements may be specified.<br/>

**Width** <br/>
-The default width of an element depends on its display value. Block-level elements have a default width of 100%, consuming the entire horizontal space available.<br/>
-Inline and inline-block elements expand and contract horizontally to accommodate their content.<br/> -Inline-level elements cannot have a fixed size, thus the width and height properties are only relevant to non-inline elements. To set a specific width for a non-inline element, use the width property.<br/>

**Height** <br/>
-The default height of an element is determined by its content. An element will expand and contract vertically as necessary to accommodate its content. To set a specific height for a non-inline element, use the height property.<br/>
-Block and inline-block elements will, however, accept the width and height properties and their corresponding values.<br/>

**Margin** <br/>
-The margin property allows us to set the amount of space that surrounds an element.<br/>
-Margins for an element fall outside of any border and are completely transparent in color.<br/>
-Margins can be used to help position elements in a particular place on a page or to provide breathing room, keeping all other elements a safe distance away.<br/>
-The padding property is very similar to the margin property; however, it falls inside of an element’s border, should an element have a border. The padding property is used to provide spacing directly within an element.<br/>

**Margin & Padding Declarations** <br/>
-The margin and padding properties come in both longhand and shorthand form. When using the shorthand margin property to set the same value for all four sides of an element, we specify one value.<br/>
-To set one value for the top & bottom and another value for the left and right sides of an element, specify two values: top and bottom first, then left and right.<br/>
-To set unique values for all four sides of an element, specify those values in the order of top, right, bottom, and left, moving clockwise.<br/>
-Using the margin or padding property alone, with any number of values, is considered shorthand. With longhand, we can set the value for one side at a time using unique properties. Each property name (in this case margin or padding) is followed by a dash and the side of the box to which the value is to be applied: top, right, bottom, or left. For example, the padding-left property accepts only one value and will set the left padding for that element; the margin-top property accepts only one value and will set the top margin for that element.<br/>

**Borders** <br/>
-Borders fall between the padding and margin, providing an outline around an element.<br/>
-The border property requires three values: width, style, and color.<br/>

**Individual Border Sides** <br/>
-As with the margin and padding properties, borders can be placed on one side of an element at a time. Doing so requires new properties: border-top, border-right, border-bottom, and border-left. The values for these properties are the same as those of the border property alone: width, style, and color.<br/>

-Additionally, styles for individual border sides may be controlled at an even finer level. For example, if we wish to change only the width of the bottom border we can use the following code.<br/>

**Border Radius** <br/>
-The border-radius property accepts length units,including percentages and pixels, that identify the radius by which the corners of an element are to be rounded. <br/>
-A single value will round all four corners of an element equally; two values will round the top-left/bottom-right and top-right/bottom-left corners in that order; four values will round the top-left, top-right, bottom-right, and bottom-left corners in that order.<br/>
-When considering the order in which multiple values are applied to the border-radius property (as well as the margin and padding properties), remember that they move in a clockwise fashion starting at the top left of an element.<br/>
