# Web Performance

## Common practice
* Set performance budgets
* Optimize your images https://web.dev/image-cdns/ 
* Lazy-load images and video
* Optimize your JavaScript
* Optimize your resource delivery
* Optimize your CSS
* Optimize your third-party resources
* Optimize WebFonts
* Optimize for network quality
* Measure performance in the field
* Build a performance culture

Read more https://web.dev/fast 

## Optimization of resource delivery
- Push (or preload) critical resources.
- Render the initial route as soon as possible.
- Pre-cache remaining assets.
- Lazy load other routes and non-critical assets.

## First Contentful Paint aka FCP
FCP performance metric marks the first point in the page load timeline where the user can see anything on the screen.
https://web.dev/fcp/

## First Meaningful Paint aka FMP
FMP is a metric for estimation pagge loading experience but it still do not identify when the main content of the page has loaded. FMP is deprecated.
https://web.dev/first-meaningful-paint/

## Large Contentful Paint aka LCP
LCP is the most relevant performance metric corresponding to what the user sees on their screen while the page is loading.
LCP provide a more accurate way of measuring page loading speed unlike [FCP](#first-contentful-paint-aka-fcp) or [FMP](#first-meaningful-paint-aka-fmp)
Source https://web.dev/largest-contentful-paint/

## Resource Timing API
This API provide a way of collecting and analyzing information about network timing data on a page.
Read more https://developer.mozilla.org/en-US/docs/Web/API/Resource_Timing_API.


`Timing-Allow-Origin Header` - http header which specify origins which from which a browser is allowed to get information about request timings via Resource Timing API.
Source https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Timing-Allow-Origin

