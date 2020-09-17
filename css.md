# CSS Questions
1. What is CSS selector specificity and how does it work?
-  CSS specificity is a set of rules used by browsers in determining which of the developer-defined styles will be applied to a specific element. For a style to be applied to a particular element, the developer has to abide by the rules, so that the browser knows how to apply the style.

2. What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
- Resetting: Removing all styling from every element - margins, padding, etc. All elements will have the same font-size, same line-height and no spacing. Eric Meyer's Reset is the most common approach: http://meyerweb.com/eric/tools/css/reset/
- Normalizing: Making elements render consistently across browsers. So all h1s will have the same size across browsers, for instance. Nicolas Gallagher's normalize.css is generally used for normalizing: http://necolas.github.io/normalize.css/
- I personally prefer normalizing a bajillion times over resetting. There's no point in resetting everything only to style it again.

3. Describe Floats and how they work.
- Float is a CSS positioning property. Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning. Absolutely positioned page elements are removed from the flow of the webpage
```css
#sidebar {
  float: right; // left right none inherit            
}
```

4. Describe z-index and how stacking context is formed.
- The Z-index is a property that allows the developer to stack elements in the CSS. It’s basically a 3-d property so it allows the developer to choose how close the element appears. This is how stacking context is formed.

5. Describe BFC (Block Formatting Context) and how it works.
- A block formatting context is a part of a visual CSS rendering of a web page. It’s the region in which the layout of block boxes occurs and in which floats interact with other elements.
Some examples I have found online on how to use block formatting context:
    - The root element of the document (<html>).
    - Floats (elements where float isn't none).
    - Absolutely positioned elements (elements where position is absolute or fixed).
    - Inline-blocks (elements with display: inline-block).
    - Table cells (elements with display: table-cell, which is the default for HTML table cells).

6. What are the various clearing techniques and which is appropriate for what context?
- Empty div method - <div style="clear:both;"></div>.
- Clearfix method — Refer to the .clearfix class above.
- overflow: auto or overflow: hidden method - Parent will establish a new block formatting context and expand to contains its floated children.
- In large projects, I would write a utility .clearfix class and use them in places where I need it. overflow: hiddenmight clip children if the children is taller than the parent and is not very ideal.