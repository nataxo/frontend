# Security

## Web Attacks
- XSS https://developer.mozilla.org/en-US/docs/Web/Security/Types_of_attacks#Cross-site_scripting_XSS 
- CSRF is an attack that forces an end user to execute unwanted actions on a web application in which they're currently authenticated
- HTTP mixed content https://web.dev/what-is-mixed-content/

## Vulnerabilities
1. User generated content
2. node_modules
3. Browser extensions

## Content Security Policy aka CSP

CSP tells the browser from which origins it can load the data for a page.
CSP can be considered as an allowed list of domain names which is generated on a server side and passed to the browser in the response header.

https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy

## Cross-Origin Resource Sharing aka CORS

Cross-Origin Resource Sharing is an HTTP-header based mechanism that allows a server to indicate any other origins (domain, scheme, or port) than its own from which a browser should permit loading of resources. 

## Preflight request

CORS relies on a mechanism by which browsers make a “preflight” request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.
Preflight request potentially can be used by fraudsters.

https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

## How to prevent 
1. Sanitize user generated content
2. Look after node_modules. Update dependencies
3. Use [CSP](#content-security-policy-aka-csp)
4. Use [CORS](#cross-origin-resource-sharing-aka-cors)
5. Use Tools for dynamic analysis - Synk, Lighthouse
6. Use EsLint for static analysis of security
   Eslint-plugin-security  https://www.npmjs.com/package/eslint-plugin-security

## Talk
https://www.youtube.com/watch?v=2gthjl2Lks4