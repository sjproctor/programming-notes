# CSS Notes


CSS - Notes from "The Hard Parts" with Amy Dutton

1. Cascade
- user-agent - browser defaults, CSS resets and CSS normalize - makes tags look consistent across browsers, user agent style sheet in italics in the dev tools
- user - can change default text size
- author - dev
  1 - inline
  2 - internal - style tag in HTML
  3 - external - stylesheet
organization (in order) - tags, layout, classes, page specific

2. Specificity
- Style attribute is most specific, the id, the class/pseudo-class/attribute, elements
- ~ sibling selector, + looks for two tags next to each other
- Use classes rather than ids

3. Positioning
- Static
- Relative - relative to the parent item, which could be the page
- Fixed - keeps the item where it is on the page regardless of scrolling, footer: `position: fixed/bottom:0`
- Absolute - collapse the space
- Sticky - stays where it is based on the container, good for header

4. Box model
- border-spacing: boarder-box, makes the width include the padding


5. Img in a card - width: 100%, height: 100%, object-fit: cover, object-position: left bottom (moves the img around within the particular size of window)
