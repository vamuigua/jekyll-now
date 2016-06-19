---
layout: post
title: Getting to Know CSS
---
**The Cascade**<br/>
-Within CSS, all styles cascade from the top of a style sheet to the bottom, allowing different styles to be added or overwritten as the style sheet progresses.<br/>
-For example, we select all paragraph elements at the top of our style sheet and set their background color to orange and their font size to 24 pixels. Then towards the bottom of our style sheet, we select all paragraph elements again and set their background color to green.For example:<br/>

    p {
      background: orange;
      font-size: 24px;
    }
    p {
      background: green;
    }

-Because the paragraph selector that sets the background color to green comes after the paragraph selector that sets the background color to orange, it will take precedence in the cascade. All of the paragraphs will appear with a green background. The font size will remain 24 pixels because the second paragraph selector didn’t identify a new font size<br/>

**Calculating Specificity**<br/>
-A selector’s specificity weight, along with its placement in the cascade, identifies how its styles will be rendered. The three different types of selectors: the type, class, and ID selectors;each of these selectors has a different specificity weight.<br/>
-The type selector has the lowest specificity weight and holds a point value of 0-0-1. The class selector has a medium specificity weight and holds a point value of 0-1-0. Lastly, the ID selector has a high specificity weight and holds a point value of 1-0-0. As we can see, specificity points are calculated using three columns. The first column counts ID selectors, the second column counts class selectors, and the third column counts type selectors.<br/>
-The higher the specificity weight of a selector, the more superiority the selector is given when a styling conflict occurs. For example, if a paragraph element is selected using a type selector in one place and an ID selector in another, the ID selector will take precedence over the type selector regardless of where the ID selector appears in the cascade.<br/>

    <p id="food">...</p>    

    #food {
    background: green;
    }
    p {
    background: orange;
    }

-Here we have a paragraph element with an id attribute value of food. Within our CSS, that paragraph is being selected by two different kinds of selectors: one type selector and one ID selector. Although the type selector comes after the ID selector in the cascade, the ID selector takes precedence over the type selector because it has a higher specificity weight; consequently the paragraph will appear with a green background.<br/>

**Combining Selectors**<br/>
-By combining selectors we can be more specific about which element or group of elements we’d like to select.<br/>
-For example, say we want to select all paragraph elements that reside within an element with a class attribute value of hotdog and set their background color to brown. However, if one of those paragraphs happens to have the class attribute value of mustard, we want to set its background color to yellow. Our HTML and CSS may look like the following:<br/>

    <div class="hotdog">
    <p>...</p>
    <p>...</p>
    <p class="mustard">...</p>
    </div>

        .hotdog p {
      background: brown;
    }
    .hotdog p.mustard {
      background: yellow;
    }

-The first combined selector above, .hotdog p, includes two selectors: a class and a type selector. These two selectors are separated by a single space. The key selector is a type selector targeting paragraph elements. And because this type selector is prequalified with a class selector of hotdog, the full combined selector will only select paragraph elements that reside within an element with a class attribute value of hotdog.<br/>
-The second selector above, .hotdog p.mustard, includes three selectors: two class selectors and one type selector. The only difference between the second selector and the first selector is the addition of the class selector of mustard to the end of the paragraph type selector. Because the  new class selector, mustard, falls all the way to the right of the combined selector, it is the key selector, and all of the individual selectors coming before it are now prequalifiers.<br/>

**Layering Styles with Multiple Classes**<br/>
-Elements within HTML can have more than one class attribute value so long as each value is space separated. With that, we can place certain styles on all elements of one sort while placing other styles only on specific elements of that sort.<br/>
-Let’s take a look at buttons, for example. Say we want all of our buttons to have a font size of 16 pixels, but we want the background color of our buttons to vary depending on where the buttons are used. We can create a few classes and layer them on an element as necessary to apply the desired styles.<br/>

    a class="btn btn-danger">...</a>
    <a class="btn btn-success">...</a>

    .btn {
      font-size: 16px;
    }
    .btn-danger {
      background: red;
    }
    .btn-success {
      background: green;
    }

**Lengths**
-Length values within CSS are similar to colors in that there are a handful of different types of values for length, all of which serve distinct purposes. Length values come in two different forms, absolute and relative, each of which uses different units of measurement.<br/>

**Absolute Lengths**<br/>
-Absolute length values are the simplest length values, as they are fixed to a physical measurement, such as inches, centimeters, or millimeters. The most popular absolute unit of measurement is known as the pixel and is represented by the px unit notation<br/>

**Pixels**<br/>
The pixel is equal to 1/96th of an inch; thus there are 96 pixels in an inch. The exact measurement of a pixel, however, may vary slightly between high-density and low-density viewing devices.The code here is using pixels to set the font size of all paragraphs to 14 pixels:<br/>

      p {
        font-size: 14px;
      }

**Relative Lengths**<br/>
-In addition to absolute length values, there are also relative length values. Relative length values are a little more complicated, as they are not fixed units of measurement; they rely on the length of another measurement.<br/>

**Percentages**<br/>
-Percentages, represented by the % unit notation, are one of the most popular relative values. Percentage lengths are defined in relation to the length of another object. For example, to set the width of an element to 50%, we have to know the width of its parent element, the element it is nested within, and then identify 50% of the parent element’s width.<br/>

    .col {
      width: 50%;
    }

-Percentages are extremely helpful for setting the height & width of elements and building out a web page’s layout. We’re going to rely on them often to help us out in these areas<br/>

**Em**
-The em unit is also a very popular relative value. The em unit is represented by the em unit notation, and its length is calculated based on an element’s font size.<br/>
-A single em unit is equivalent to an element’s font size. So, for example, if an element has a font size of 14 pixels and a width set to 5em, the width would equal 70 pixels (14 pixels multiplied by 5).<br/>

      banner {
        font-size: 14px;
        width: 5em;
      }
