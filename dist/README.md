# Website Performance Optimization portfolio project

In this project, badly performing portfolio site is optimized for fast loading and rendering.

## How to use

Clone or Download from the [FEND-WebsiteOptimization repository](https://github.com/kwonjh90/FEND-WebsiteOptimization/) and run index.html.

## Project specifications, results, and list of changes
### A. Critical Rendering Path
  **A.1 Specification: index.html achieves a PageSpeed score of at least 90 for Mobile and Desktop.**
  **Optimized Performance: 96/100 on Mobile and 98/100 on Desktop**
  **Optimizations made:**
  1. Removed Google Font.
  2. Inlined two CSS files (style.css and print.css).
  3. Async google-analytics.JS.
  4. Optimized image files using [GiftOfSpeed](https://www.giftofspeed.com/jpg-compressor/).
  5. Minified HTML file using.

### B. Getting Rid of Jank
  **B.1 Specification: Optimizations made to views/js/main.js make views/pizza.html render with a consistent frame-rate at 60fps when scrolling.**
  **Optimized Performance: ~800fps (~1.25 ms/frame)**
  **Optimizations made:**
  1. Moved a number of variables (`items`, `phase`, `top`) outside the for loop to prevent it being invoked on every iteration.
  2. Implemented `style.transform = "translateX()"` to prevent repaints.
  3. Moved a number of variables (`elem,` `document.getElementById("movingPizzas1")`) outside the for loop to prevent.
  4. Decreased the number of pizzas. Made the number depend on the screen size.
  5. Positioned pizzas using %.
  6. Optimized image files using [GiftOfSpeed](https://www.giftofspeed.com/jpg-compressor/).
  7. Minified HTML, CSS, Java Script files.


  **B.2 Specification: Time to resize pizzas is less than 5 ms using the pizza size slider on the views/pizza.html page. Resize time is shown in the browser developer tools.**
  **Optimized Performance:** ~0.45 ms
  **Optimizations made:**
  1. Replaced `querySelector` with `getElementById`.
  2. Moved "document.querySelectorAll(".randomPizzaContainer").length" outside the for loop to prevent it being invoked on every iteration.
  3. Resized pizzas using %
  4. Moved `document.getElementById("randomPizzas")` outside the for loop to prevent it being invoked on every iteration.
  5. Optimized image files using [GiftOfSpeed](https://www.giftofspeed.com/jpg-compressor/).
  6. Minified HTML, CSS, Java Script files.

## Future Goals
* Implement additional recommendations from previous feedback.
  1. Apply 'use strict' on views/js/main.js.
  2. Apply hidden on views/css/style.css.
* Implement additional recommendations from [PageSpeed](https://developers.google.com/speed/pagespeed/insights/).
  1. Reduce server response time.
  2. Leverage browser caching.
* Beautify some more the currently optimized portfolio.
  1. Fix moving pizzas overlapping when the screen size is decreased.
