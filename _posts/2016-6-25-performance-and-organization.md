---
layout: post
title: Performance & Organization in Website Development
---
**Performance & Organization.**<br/>
-The first part to improving a website’s performance and organization revolves around identifying a good strategy and structure for developing the code base.<br/>
**Style Architecture**<br/>
-Exactly how to organize styles boils down to personal preference and what is best for a given website but generally speaking there are best practices to follow. One practice includes separating styles based on intent, which includes creating directories for common base styles, user interface components, and business logic modules.<br/>

              # Base
                – normalize.css
                – layout.css
                – typography.css

              # Components
                – alerts.css
                – buttons.css
                – forms.css
                – list.css
                – nav.css
                – tables.css

              # Modules
                – aside.css
                – footer.css
                – header.css

-The architecture outlined above includes three directories, all with individual groups of styles. The goal here is to start thinking of websites as systems rather than individual pages, and the code architecture should reflect this mindset.<br/>
-The base directory includes common styles and variables to be used across the entire website, layout and typography styles for example. The components directory includes styles for specific user interface elements which are broken down into different component files such as alerts and buttons. Lastly, the modules directory includes styles for different sections of a page, which are determined by business needs.<br/>

**OBJECT ORIENTED CSS**
-Object Oriented CSS identifies two principles that will help build scalable websites with a strong architecture and a reasonable amount of code. These two principles include:<br/>
<ul>
   <li>Separate structure from skin</li>
   <li>Separate content from container</li>
</ul>

-Overall separating structure from skin includes abstracting the layout of an element away from the theme of a website. The structure of a module should be transparent, allowing other styles to be inherited and displayed without conflict. Most commonly this requires a solid grid and layout structure, along with well crafted modules.<br/>
-Separating content from the container involves removing the dependency of a parent element nesting children elements. A heading should look the same regardless of its parent container. To accomplish this, elements need to inherent default styles, then be extended with multiple classes as necessary.<br/>  

             HTML
          <div class="alert alert-error">
            <p class="msg">...</p>
          </div>


              CSS
            .alert {...}
            .alert-error {...}
            .msg {...}

**Scalable & Modular Architecture for CSS**
-The Scalable and Modular Architecture for CSS promotes breaking up styles into five core categories, including:<br/>
<ul>
            <li>Base</li>
            <li>Layout</li>
            <li>Module<li/>
            <li>State</li>
            <li>Theme</li>
</ul>

-The base category includes core element styles, covering the general defaults. The layout category then identifies the sizing and grid styles of different elements, determining their layout. Module styles are more specific styles targeting individual parts of the page, such as navigation or feature styles.<br/>
-The state styles are then used to augment or override other styles in the event that a module includes an alternate state, an active tab for example.<br/>
-Lastly, the theme category may be added which could include styles based around the skin, or look and feel, of different modules.<br/>
