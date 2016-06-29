---
layout: post
title: Complex Selectors
---
**Complex Selectors**<br/>
**COMMON SELECTORS**<br/>
With an Example:<br/>
<ul>
<li>h1 - A Type Selector-Selects an element by it’s type</li>
<li>.tagline - A Class Selector-Selects an element by the class attribute value, which may be reused multiple times per page</li>
<li>#intro - ID Selector-Selects an element by the ID attribute value, which is unique and to only be used once per page</li>
</ul>

**Child Selectors**<br/>
-Child selectors provide a way to select elements that fall within one another, thus making them children of their parent element. These selections can be made two different ways, using either descendant or direct child selectors.<br/>

**1.Descendant Selector**<br/>
It matches every element that follows an identified ancestor. The descendant element does not have to come directly after the ancestor element inside the document tree, such as a parent-child relationship, but may fall anywhere within the ancestor element. Descendant selectors are created by spacing apart elements within a selector, creating a new level of hierarchy for each element list.<br/>

          CSS
          article h2 {...}

          HTML
          <h2>...</h2>
          <article>
            <h2>This heading will be selected</h2>
            <div>
              <h2>This heading will be selected</h2>
            </div>
          </article>

**2.Direct Child Selector**
At times only the direct children of a parent element need to be selected, not every instance of the element nested deeply inside of an ancestor. In this event the direct child selector may be used by placing a greater than sign, >, between the parent element and child element within the selector.
E.g Below, the paragraph on line 3 is the only direct child of it’s parent article, thus selected.

          CSS
          article > p {...}

          HTML
          <p>...</p>
          <article>
            <p>This paragraph will be selected</p>
            <div>
              <p>...</p>
            </div>
          </article>

Sibling Selectors
1.General Sibling Selector          
The general sibling selector allow elements to be selected based on their sibling elements, those which share the same common parent. They are created by using the tilde character, ~, between two elements within a selector. The first element identifies what the second element shall be a sibling with, and both of which must share the same parent
E.g The paragraphs on lines 5 and 9 are selected as they come after the heading within the document tree and share the same parent as their sibling heading.

              CSS
              h2 ~ p {...}

              HTML
              <p>...</p>
              <section>
                <p>...</p>
                <h2>...</h2>
                <p>This paragraph will be selected</p>
                <div>
                  <p>...</p>
                </div>
                <p>This paragraph will be selected</p>
              </section>

2.Adjacent Sibling Selector
The adjacent sibling selector will only select sibling elements directly following after another sibling element. Instead of using the tilde character, as with general sibling selectors, the adjacent sibling selector uses a plus character, +, between the two elements within a selector. Again, the first element identifies what the second element shall directly follow after and be a sibling with, and both of which must share the same parent.
E.g The paragraph on line 5 is selected as it directly follows after its sibling heading along with sharing the same parent element, thus selected.

                CSS
                h2 + p {...}

                HTML
                <p>...</p>
                <section>
                  <p>...</p>
                  <h2>...</h2>
                  <p>This paragraph will be selected</p>
                  <div>
                    <p>...</p>
                  </div>
                  <p>...</p>
                </section>

Pseudo-classes
1.Link Pseudo-classes
Some of the more basic pseudo-classes include two revolving around links specifically. The :link and :visited pseudo-classes define if a link has or hasn’t been visited. To style an anchor which has not been visited the :link pseudo-class comes into play, where the :visited pseudo-class styles links that a user has already visited based on their browsing history.
                a:link {...}
                a:visited {...}

2.User Action Pseudo-classes
Based on a users actions different pseudo-classes may be dynamically applied to an element, of which include the :hover, :active, and :focus pseudo-classes. The :hover pseudo-class is applied to an element when a user moves their cursor over the element, most commonly used with anchor elements. The :active pseudo-class is applied to an element when a user engages an element, such as clicking on an element. Lastly, the :focus pseudo-class is applied to an element when a user has made an element the focus point of the page, often by using the keyboard to tab from one element to another.                
                a:hover {...}
                a:active {...}
                a:focus {...}

3.User Interface State Pseudo-classes
The :enabled pseudo-class selects an input that is in the default state of enabled and available for use, where the :disabled pseudo-class selects an input that has the disabled attribute tied to it. Many browsers by default will fade out disabled inputs to inform users that the input is not available for interaction, however those styles may be adjusted as wished with the :disabled pseudo-class.

                input:enabled {...}
                input:disabled {...}

The last two user interface element state pseudo-classes of :checked and :indeterminate revolve around checkbox and radio button input elements. The :checked pseudo-class selects checkboxes or radio buttons that are, as you may expect, checked. When a checkbox or radio button has neither been selected or unselected it lives in an indeterminate state, from which the :indeterminate pseudo-class can be used to target these elements.

                input:checked {...}
                input:indeterminate {...}
