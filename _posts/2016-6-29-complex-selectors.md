---
layout: post
title: Complex Selectors
---
Complex Selectors
COMMON SELECTORS
With an Example:
 h1 - A Type Selector-Selects an element by it’s type
 .tagline - A Class Selector-Selects an element by the class attribute value, which may be reused multiple times per page
 #intro - ID Selector-Selects an element by the ID attribute value, which is unique and to only be used once per page

 Child Selectors
Child selectors provide a way to select elements that fall within one another, thus making them children of their parent element. These selections can be made two different ways, using either descendant or direct child selectors.

1.Descendant Selector
It matches every element that follows an identified ancestor. The descendant element does not have to come directly after the ancestor element inside the document tree, such as a parent-child relationship, but may fall anywhere within the ancestor element. Descendant selectors are created by spacing apart elements within a selector, creating a new level of hierarchy for each element list.

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

2.Direct Child Selector
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

Attribute Selectors
1.Attribute Present Selector
The first attribute selector identifies an element based on whether it includes an attribute or not, regardless of any actual value. To select an element based on if an attribute is present or not simply include the attribute name in square brackets, [], within a selector. The square brackets may or may not follow any qualifier such as an element type or class, all depending on the level of specificity desired.
