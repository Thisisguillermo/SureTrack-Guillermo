# CSS Unites https://www.freecodecamp.org/news/css-unit-guide/

Common Length units

But before we start it actually depends on what you want, there's no good or bad. (Read the whole document Guillermo)

There are several units used by CSS to express length. The older ones, supported by all browsers, are:

**rem**
rem - “r” stands for “root”: “root em” -, which is equal to the font size fixed to the root element (almost always <html>).

**vh and vw**
vh and vw - Many responsive web design techniques rely heavily on percentage rules. However, CSS percentage measures are not always the best solution for all problems. The measure vh is equal to 1/100 of the height of the viewport. So, for example, if the height of the browser is 800px, 1vh equals 8px and, similarly, if the width of the viewport is 650px, 1vw is equivalent to 6.5px.

**vmin and vmax**
vmin and vmax - These units are related to the maximum or minimum value of vh and vw. For example, if the browser was set to 1200px wide and the height 600px, 1vmin would be 6px and 1vmax would be 12px. However, if the width was set to 700px and the height set to 1080px, vmin would equal 7px and vmax 10.8px.

**ex and ch**
ex and ch - These units, similar to em and rem, rely on the current font and font size. However, unlike em and rem, these units also rely on font-family as they are determined based on measures specific to each font. The ch unit (“character unit”) is defined as the width of the character zero (“0”). The ex unit is defined as “the current x-height of the current font or the half of 1em”. The height-x of a given font is the height of the lowercase “x” of that font. It is often the middle mark of the font.

## CSS "Style guide" https://www.reddit.com/r/css/comments/kzkthl/what_units_do_you_use_px_vw_and_vh_em_rem/

**px** for borders and box shadows; it's for decoration it's not required for readability.
If a user sets a very large font size for themself, you don't necessarily want this stuff cluttering up the screen.

**rem** rem for font size, don't want the font size of a parent component changing my sizes on one that's inside.
**rem** also used for padding and margins

**vw/vh** for things that need to change with the size of the screen.
*A caveat for something that has width: 100vw; height: 100vh. The viewport units DON'T take scrollbars into account. So if you do the above and have a vertical scrollbar because of content overflow, you'll also get a horizontal scrollbar that scrolls the exact width of the vertical scrollbar. In this case, often width: 100%; height: 100vh; might work.*

**ch**
*ch is a great unit. Studies have shown in the past that it's easiest for humans to read paragraphs that are between 50-70 letters across in width. So I often have a rule of something like p { width: 60ch; } or similar.*


## Thoughts and comments

https://gist.github.com/basham/2175a16ab7c60ce8e001

https://graphicdesign.stackexchange.com/questions/153807/why-would-i-ever-not-use-percentage-for-sizes



### Pixel based media queries in Safari desktop and mobile.

*Pixel based media queries are out of the question. Safari doesn’t support them properly (unless you decide to forsake Safari?).*

https://zellwk.com/blog/media-query-units/


*For most users (and browsers), a font-size of 100% would default to 16px unless they change the default font-size through their browser settings. It’s rare that anyone would do that though."*

https://zellwk.com/blog/rem-vs-em/

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Container_Queries

### Devices resolution

https://yesviz.com/devices.php