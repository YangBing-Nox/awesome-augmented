<h1>
 Critical-path (Above-the-fold) CSS Tools
 <a href="https://github.com/sindresorhus/awesome">
  <img alt="Awesome" src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg"/>
 </a>
</h1>
<blockquote>
 <p>
  Tools to help prioritize above-the-fold CSS
 </p>
</blockquote>
<h3>
 Prioritize above-the-fold content first.
</h3>
<p>
 For best performance, PageSpeed Insights
 <a href="https://developers.google.com/speed/docs/insights/PrioritizeVisibleContent">
  recommends
 </a>
 inlining the critical (above-the-fold) CSS of your page directly into your HTML. This eliminates additional roundtrips and allows the browser to paint the above-fold experience to your user's screen sooner. The main idea is:
</p>
<ul>
 <li>
  Determine the above-the-fold styles for a page and write them between
  <code>
   <style>
  </code>
  tags in the head.
 </li>
 <li>
  Load all other stylesheets in the footer, ideally asynchronously.
 </li>
</ul>
<p>
 The following is a list of tools to help generate, inline and report on critical-path CSS.
</p>
<h2>
 Node modules
</h2>
<ul>
 <li>
  <a href="https://github.com/pocketjoso/penthouse">
   Penthouse
  </a>
  - by Jonas Ohlsson generates critical-path CSS
  <sup>
   &#9733 1212, pushed 130 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/addyosmani/critical">
   Critical
  </a>
  - by Addy Osmani generates & inlines critical-path CSS (uses Penthouse,
  <a href="https://github.com/addyosmani/oust">
   Oust
  </a>
  and inline-styles)
  <sup>
   &#9733 3120, pushed 137 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/filamentgroup/criticalcss">
   CriticalCSS
  </a>
  - by FilamentGroup finds & outputs critical CSS
  <sup>
   &#9733 679, pushed 147 days ago
  </sup>
 </li>
</ul>
<h2>
 Server-side modules
</h2>
<ul>
 <li>
  <a href="https://github.com/pagespeed/mod_pagespeed">
   mod_pagespeed
  </a>
  - Apache module for automatic PageSpeed optimization
  <sup>
   &#9733 225, pushed 129 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/pagespeed/ngx_pagespeed">
   ngx_pagespeed
  </a>
  - Nginx module for automatic PageSpeed optimization
  <sup>
   &#9733 3011, pushed 129 days ago
  </sup>
 </li>
</ul>
<h2>
 Grunt tasks
</h2>
<ul>
 <li>
  <a href="https://github.com/fatso83/grunt-penthouse">
   grunt-penthouse
  </a>
  <sup>
   &#9733 64, pushed 197 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/filamentgroup/grunt-criticalcss">
   grunt-critical-css
  </a>
  <sup>
   &#9733 506, pushed 210 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/bezoerb/grunt-critical">
   grunt-critical
  </a>
  <sup>
   &#9733 81, pushed 252 days ago
  </sup>
 </li>
</ul>
<h2>
 CasperJS
</h2>
<ul>
 <li>
  <a href="https://github.com/ibrennan/critical-css-casperjs">
   critical-css-casperjs
  </a>
  - CasperJS script to pull critical CSS information from pages
  <sup>
   &#9733 68, pushed 888 days ago
  </sup>
 </li>
</ul>
<h2>
 PhantomJS
</h2>
<ul>
 <li>
  <a href="https://github.com/drdk/dr-css-inliner">
   dr-css-inliner
  </a>
  - PhantomJS script to inline above-the-fold CSS on a page.
  <sup>
   &#9733 58, pushed 727 days ago
  </sup>
 </li>
</ul>
<h2>
 Inline sources (styles, scripts)
</h2>
<ul>
 <li>
  <a href="https://github.com/maxogden/inline-styles">
   inline-styles
  </a>
  - by Max Ogden, replaces
  <code>
   <link>
  </code>
  tags with inline
  <code>
   <style>
  </code>
  tags + inlines CSS url() calls with data URIs
  <sup>
   &#9733 21, pushed 777 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/fmal/gulp-inline-source">
   gulp-inline-source
  </a>
  - by Filip Malinowski, replaces
  <code>
   <link>
  </code>
  tags with inline
  <code>
   <style>
  </code>
  tags, and replaces
  <code>
   <script src="">
  </code>
  tags with their inline content
  <sup>
   &#9733 97, pushed 407 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/bezoerb/inline-critical">
   inline-critical
  </a>
  - by Ben Zörb, inline critical path CSS and load existing stylesheets with
  <code>
   loadCSS
  </code>
  <sup>
   &#9733 39, pushed 129 days ago
  </sup>
 </li>
 <li>
  <a href="https://github.com/kriasoft/isomorphic-style-loader/">
   isomorphic-style-loader
  </a>
  for Webpack - allows to extract critical CSS for any given page/screen in React apps and inline it into HTML during server-side rendering (SSR). See
  <a href="https://github.com/kriasoft/react-starter-kit">
   React Starter Kit
  </a>
  as an example.
 </li>
</ul>
<h2>
 Async load CSS
</h2>
<p>
 Async loading should be used to fetch the rest of your site-wide styles after you've inlined your critical-path CSS.
</p>
<ul>
 <li>
  <a href="https://github.com/filamentgroup/loadCSS">
   loadCSS
  </a>
  - loads CSS asynchronously using JS.
  <a href="https://gist.github.com/scottjehl/87176715419617ae6994">
   Research
  </a>
  that led to this is also available.
  <sup>
   &#9733 3130, pushed 144 days ago
  </sup>
 </li>
 <li>
  <a href="https://gist.github.com/matt-bailey/602b40c77a5d3381ff26">
   async & conditional loading
  </a>
  - POC script for loading CSS files asynchronously and conditionally based on body tag classes
 </li>
 <li>
  <a href="https://github.com/n0mad01/asyncLoader">
   asyncLoader
  </a>
  - async script/stylesheet loader
  <sup>
   &#9733 0, pushed 620 days ago
  </sup>
 </li>
 <li>
  <a href="http://addyosmani.github.io/basket.js/">
   basket.js
  </a>
  - async script/resource loader with support for localStorage caching. Can be
  <a href="https://github.com/andrewwakeling/basket-css-example">
   extended
  </a>
  to load stylesheets.
 </li>
</ul>
<p>
 Note: The Guardian currently also cache their global styles into localStorage for subsequent page loads. More info in this
 <a href="https://gist.github.com/scottjehl/87176715419617ae6994">
  comment
 </a>
 .
</p>
<h2>
 Online tools
</h2>
<ul>
 <li>
  <a href="https://jonassebastianohlsson.com/criticalpathcssgenerator/">
   Penthouse online
  </a>
 </li>
</ul>
<h2>
 Bookmarklets/Extensions
</h2>
<ul>
 <li>
  <a href="https://gist.github.com/PaulKinlan/6284142">
   Snippet
  </a>
  by Paul Kinlan. Patrick Hamann has an
  <a href="http://patrickhamann.com/workshops/performance/tasks/2_Critical_Path/2_2.html">
   exercise
  </a>
  using the snippet you can try out.
 </li>
 <li>
  <a href="https://gist.github.com/scottjehl/b6129da04733e4e0f9a4">
   Snippet
  </a>
  by Scott Jehl
 </li>
 <li>
  <a href="https://github.com/ndreckshage/CSSVacuum">
   CSSVacuum
  </a>
  by ndreckshage
  <sup>
   &#9733 33, pushed 1089 days ago
  </sup>
 </li>
</ul>
<h2>
 Render-blocking issues detection
</h2>
<ul>
 <li>
  <a href="https://developers.google.com/speed/pagespeed/insights/">
   PageSpeed Insights
  </a>
  - Online tool that measures the performance of a page for mobile devices and desktop devices. It fetches the url twice, once with a mobile user-agent, and once with a desktop-user agent.
 </li>
 <li>
  <a href="https://github.com/addyosmani/psi">
   PSI
  </a>
  - Node module for PageSpeed Insights reporting as part of your build process. Use directly with Gulp or use
  <a href="https://github.com/jrcryer/grunt-pagespeed">
   grunt-pagespeed
  </a>
  if a Grunt user. For local testing, a write-up using this task and
  <a href="http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/">
   ngrok
  </a>
  is available.
  <sup>
   &#9733 2125, pushed 150 days ago
  </sup>
 </li>
 <li>
  <a href="https://chrome.google.com/webstore/detail/pagespeed-insights-by-goo/gplegfbjlmmehdoakndmohflojccocli?hl=en">
   PageSpeed Insights DevTools extension
  </a>
  - Chrome extension for running PageSpeed tests from inside the browser.
 </li>
 <li>
  <a href="https://chrome.google.com/webstore/detail/pagespeed-insights-checke/mkjmodmicmpjedhoekkmafdgpocdkbna?hl=en">
   PageSpeed Insights Checker for mobile extension
  </a>
  - checks Mobile PageSpeed score for every page and gives you a handy preview.
 </li>
</ul>
<h2>
 Supplementary tools
</h2>
<ul>
 <li>
  <a href="https://github.com/giakki/uncss">
   UnCSS
  </a>
  removes unused CSS from pages, allowing you to reduce the global CSS you may need to load in for your site. Tasks are available for
  <a href="https://github.com/addyosmani/grunt-uncss">
   Grunt
  </a>
  ,
  <a href="https://github.com/ben-eb/gulp-uncss">
   Gulp
  </a>
  and
  <a href="https://addyosmani.com/blog/removing-unused-css/">
   other
  </a>
  build tools.
  <sup>
   &#9733 3684, pushed 130 days ago
  </sup>
 </li>
</ul>
