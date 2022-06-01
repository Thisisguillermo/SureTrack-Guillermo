TailwindCSS Style Guide Guillermo

``` html

## Padding, max screen width, margin, background-colour, style (e.g. rounded corners) aligning items

<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
  <div class="shrink-0">
    <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div>
    <div class="text-xl font-medium text-black">ChitChat</div>
    <p class="text-slate-500">You have a new message!</p>
  </div>
</div>

div class="py-8 px-8 max-w-sm mx-auto bg-white rounded-xl shadow-lg space-y-2 sm:py-4 sm:flex sm:items-center sm:space-y-0 sm:space-x-6">
  <img class="block mx-auto h-24 rounded-full sm:mx-0 sm:shrink-0" src="/img/erin-lindford.jpg" alt="Woman's Face">
  <div class="text-center space-y-2 sm:text-left">
    <div class="space-y-0.5">
      <p class="text-lg text-black font-semibold">
        Erin Lindford
      </p>
      <p class="text-slate-500 font-medium">
        Product Engineer
      </p>
    </div>
    <button class="px-4 py-1 text-sm text-purple-600 font-semibold rounded-full border border-purple-200 hover:text-white hover:bg-purple-600 hover:border-transparent focus:outline-none focus:ring-2 focus:ring-purple-600 focus:ring-offset-2">Message</button>
  </div>
</div>

<form>
  <label class="block">
    <span class="block text-sm font-medium text-slate-700">Username</span>
    <!-- Using form state modifers, the classes can be identical for every input -->
    <input type="text" value="tbone" disabled class="mt-1 block w-full px-3 py-2 bg-white border border-slate-300 rounded-md text-sm shadow-sm placeholder-slate-400
      focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500
      disabled:bg-slate-50 disabled:text-slate-500 disabled:border-slate-200 disabled:shadow-none
      invalid:border-pink-500 invalid:text-pink-600
      focus:invalid:border-pink-500 focus:invalid:ring-pink-500
    "/>
  </label>
  <!-- ... -->
</form>

## https://tailwindcss.com/docs/hover-focus-and-other-states#styling-based-on-parent-state

<a href="#" class="group block max-w-xs mx-auto rounded-lg p-6 bg-white ring-1 ring-slate-900/5 shadow-lg space-y-3 hover:bg-sky-500 hover:ring-sky-500">
  <div class="flex items-center space-x-3">
    <svg class="h-6 w-6 stroke-sky-500 group-hover:stroke-white" fill="none" viewBox="0 0 24 24"><!-- ... --></svg>
    <h3 class="text-slate-900 group-hover:text-white text-sm font-semibold">New project</h3>
  </div>
  <p class="text-slate-500 group-hover:text-white text-sm">Create a new project from a variety of starting templates.</p>
</a>
```

### Mobile first

Please start designing on Mobile screen first before Desktop. Adding more changes is a lot more easier compared to hiding/removing things on smaller screens.

If confused, read https://tailwindcss.com/docs/responsive-design#mobile-first. The documentation already did great on explaining why.

### Adding font family (local)

tailwind.config.js

``` js
theme: {
    extend: {
      fontFamily: {
        'Cadillac_Sans_A': ["Cadillac Sans A;"],
      }
    },
  },
```

global.css

```css
@layer base {
  @font-face {
    font-family: 'Cadillac Sans A';
    src: url('../fonts/CadillacSansA-SemiBold.eot');
    src: local('Cadillac Sans A SemiBold'), local('CadillacSansA-SemiBold'),
      url('../fonts/CadillacSansA-SemiBold.eot?#iefix') format('embedded-opentype'),
      url('../fonts/CadillacSansA-SemiBold.woff') format('woff'),
      url('../fonts/CadillacSansA-SemiBold.ttf') format('truetype');
    font-weight: 600;
    font-style: normal;
  }
```

*.jsx

"font-" needs to in front of your custom font-family to "activate".
```jsx
<main className="text-white bg-stone-400 font-Cadillac_Sans_A font-light">
```

https://redpixelthemes.com/blog/use-custom-fonts-tailwindcss/