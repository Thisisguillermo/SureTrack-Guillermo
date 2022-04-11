# Web development

## The baseline for web development in 2022 (https://engineering.linecorp.com/en/blog/the-baseline-for-web-development-in-2022/)

*TL;DR:The baseline for web development in 2022 is: low-spec Android devices in terms of performance, Safari from two years before in terms of Web Standards, and 4G in terms of networks. The web in general is not answering those needs properly, especially in terms of performance where factors such as an over-dependence on JavaScript are hindering our sites’ performance.*

We’re not answering to the users’ needs: Especially in terms of performance and a11y.
We’re overusing JS: Both in our dependencies and in our own code.
We’re underusing HTML and CSS: This is partly due to IE support, but now that we don’t need to support IE there are many features that become usable.

If you can do something using CSS use CSS: There are many things that previously were only achievable using JS that can be done with only CSS nowadays. By doing that you can partly reduce your JS code.

Evaluate your toolset: Many newer tools have better performance baselines compared to older ones, and not every project needs to be an SPA. Some of the non-framework-based SSGs like Hugo, Jekyll, or 11ty work great for those use cases.

Build for modern browsers: Drop IE support and set your build target to ES 2017 or even 2018. Just doing that might get you bundle size improvements of up to 20%.
Consider a11y from the beginning: Having a11y in mind from the planning and design stages is the ideal scenario. Starting by improving things such as contrast rates, font sizes, semantic HTML usage, and keyboard navigation can make a great difference.

## Miscellaneous

Understanding pixels and other CSS units
https://webplatform.github.io/docs/tutorials/understanding-css-units/

## Web design

https://webflow.com/designer


https://www.editorx.com/


https://www.figma.com/

## ​​Design Languages

Airbnb: https://airbnb.design/building-a-visual-language/
Apple: https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/adaptivity-and-layout/
Atlassian: https://atlassian.design/guidelines/product/overview
Alibaba: https://ant.design/docs/spec/introduce
Microsoft: https://developer.microsoft.com/en-us/windows/apps/design
Audi: https://www.audi.com/ci/en/guides/user-interface/introduction.html
Uber: https://developer.uber.com/docs/riders/guides/design-guidelines

https://blog.marvelapp.com/motion-creates-emotion/

## HTML/CSS/JS Notes

### TIL that you're not supposed to put external links in your <nav> elements.
TL;DR: Only use nofollow if you actively think the destination doesn't deserve Google's attention. Use noopener and/or noreferrer for security.
*So if it's another website I control and want to endorse, I leave the link bare?*
*Yes, definitely.*

###  Inverted Triangle CSS (https://developer.helpscout.com/seed/glossary/itcss/)

As the name implies, your CSS code-base is to be organized in an upside-down triangle based on specificity. In other words, your super basic general styles rules should be added first, and your incredibly, perhaps obnoxiously, specific rules and overrides should be added last.

Note: Tools are specific to pre/post-processing languages like Sass or PostCSS, as mixins and functions aren’t supported in native CSS.

Settings – Variable configurations for things like colors, fonts, sizes, etc…
Tools – Globally used mixins and functions.
Generic – CSS resets and normalizing rules to create a foundation for your styles.
Elements – Style rules for bare HTML elements (like h1 or button).
Objects – Style rules for elements responsible for layout or structuring.
Components – Style rules for UI components.
Trumps – Helper or utility rules that tweak Objects or Components by adjusting and override existing rules.

### BEM Blocks, elements, and modifiers form the patterns that the BEM convention uses for naming CSS rules. (https://developer.helpscout.com/seed/glossary/bem/)

BEM is a CSS naming convention designed to emphasize relationships among CSS style rules.


### Test-driven development (https://www.wikiwand.com/en/Test-driven_development)

Unit testing

https://stackoverflow.com/questions/652292/what-is-unit-testing-and-how-do-you-do-it

#### Untit testing framework

https://www.wikiwand.com/en/List_of_unit_testing_frameworks


### React

`ReactJS` is a JavaScript library, supporting both front-end web and being run on a server, for building user interfaces and web applications. It follows the concept of reusable components.

`React Native` is a mobile framework that makes use of the JavaScript engine available on the host, allowing you to build mobile applications for different platforms (iOS, Android, and Windows Mobile) in JavaScript that allows you to use ReactJS to build reusable components and communicate with native components further explanation

Both follow the JSX syntax extension of JavaScript. Which compiles to React.createElement calls under the hood. JSX in-depth

#### Bundles for Webdevelopment

https://webpack.github.io/

First of all, what is a JavaScript bundler? A JavaScript bundler is a tool that puts your code and all its dependencies together in one JavaScript file. There are many of them out there these days, being the most popular ones browserify and webpack.

Why do we need that? Well, the underlying problem is handling dependencies in frontend code. Historically JavaScript hasn’t had a standard for requiring dependencies from your code. There was no `import` or `require` statements. Now we have the new ES2015 import statement, but let’s ignore it for now because it is not widely implemented.


#### HTML5 Boilerplate (https://www.npmjs.com/package/html5-boilerplate)

HTML5 Boilerplate is a professional front-end template for building fast, robust, and adaptable web apps or sites.

`npx create-html5-boilerplate new-site`


#### What are NPM, Yarn, Babel, and Webpack; and how to properly use them? (https://medium.com/front-end-weekly/what-are-npm-yarn-babel-and-webpack-and-how-to-properly-use-them-d835a758f987)


*NPM stands for Node Package Manager. It is what its name describes. It is a package manager for Node based environments. It keeps track of all the packages and their versions and allows the developer to easily update or remove these dependencies. All of these external dependencies are being stored inside a file called called package.json. The initial file can be created easily using CLI npm init (assuming NodeJS is installed in the system). When you install a package using NPM, the packages get downloaded from a dedicated registry. There are lot of features of NPM like publishing. If you like to learn more about NPM, check out the links at the bottom.*

*Every language that we use has some form of package manager, either official or a 3rd party one. PHP has Composer, Python has PIP/Pipenv, Java has Gradle etc.*

*Now, let’s talk briefly about Yarn. It is a package manager that uses NPM registry as its backend. Yarn has two main advantages over NPM. Firstly, Yarn creates a yarn.lock file. This file stores the exact versions of dependencies to the last digit. When installing, Yarn first checks the lock file for the versions, then checks package.json file. NPM has a shrinkwrap command that does exactly this. However, Yarn creates and updates its lock file automatically when dependencies are being installed/updated. Secondly, Yarn is very fast. When installing dependencies for a project, NPM installs packages sequentially. This slows down the performance significantly. Yarn solves this problem by installing these packages in parallel.*

*Webpack is a modular build tool that has two sets of functionality — Loaders and Plugins. Loaders transform the source code of a module. For example, style-loader adds CSS to DOM using style tags. sass-loader compiles SASS files to CSS. babel-loader transpiles JS code given the presets. Plugins are the core of Webpack. They can do things that loaders can’t. For example, there is a plugin called UglifyJS that minifies and uglifies the output of webpack.*

`sudo npm install -g yarn`

`yarn add --dev webpack @babel/core babel-loader @babel/preset-env node-sass css-loader sass-loader style-loader postcss-loader autoprefixer`


#### Webdev CSS


##### CSS Unites https://www.freecodecamp.org/news/css-unit-guide/

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

##### CSS "Style guide" https://www.reddit.com/r/css/comments/kzkthl/what_units_do_you_use_px_vw_and_vh_em_rem/

**px** for borders and box shadows; it's for decoration it's not required for readability.
If a user sets a very large font size for themself, you don't necessarily want this stuff cluttering up the screen.

**rem** rem for font size, don't want the font size of a parent component changing my sizes on one that's inside.
**rem** also used for padding and margins

**vw/vh** for things that need to change with the size of the screen.
*A caveat for something that has width: 100vw; height: 100vh. The viewport units DON'T take scrollbars into account. So if you do the above and have a vertical scrollbar because of content overflow, you'll also get a horizontal scrollbar that scrolls the exact width of the vertical scrollbar. In this case, often width: 100%; height: 100vh; might work.*

**ch**
*ch is a great unit. Studies have shown in the past that it's easiest for humans to read paragraphs that are between 50-70 letters across in width. So I often have a rule of something like p { width: 60ch; } or similar.*


##### Thoughts and comments

https://gist.github.com/basham/2175a16ab7c60ce8e001

https://graphicdesign.stackexchange.com/questions/153807/why-would-i-ever-not-use-percentage-for-sizes



##### Pixel based media queries in Safari desktop and mobile.

*Pixel based media queries are out of the question. Safari doesn’t support them properly (unless you decide to forsake Safari?).*

https://zellwk.com/blog/media-query-units/


*For most users (and browsers), a font-size of 100% would default to 16px unless they change the default font-size through their browser settings. It’s rare that anyone would do that though."*

https://zellwk.com/blog/rem-vs-em/

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Container_Queries

##### Devices resolution

https://yesviz.com/devices.php

#### Webdev stylguides

