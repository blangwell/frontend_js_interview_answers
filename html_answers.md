## what does doctype do?

Doctype lets the browser know what type of document to expect. \
HTML 5 / HTML 4 / XHTML

## How do you serve a page with content in multiple languages?

You should always use an initial language attribute in the html element. 
The language will be inherited by the other elements in the document.
```html
<!-- example -->
<html lang="en>
```
If you'd like to add pieces of text in another language while still maintaining the default language specified in the HTML, you can wrap that content in a `<span>` tag/

The Google Translate API is often used to allow users to dynamically change the language on a website. https://cloud.google.com/translate/

You can also perform a manual translation aka _localizing_ and have individual landing pages for each supported language. Similarly, you can also manually translate the entire site. You would use a _detection code_ to automatically direct a user to the appropriate language. Additionally you can create a button/link that navigates to translated versions of your site content. 

## What kind of things must you be wary of when designing or developing for multilingual sites?
It is important to make sure that you allow the user to visualize where to change the language of the page. Say you are an English speaker traveling abroad in China. You access a site that is rendered in Chinese. Best practices would be to have a clear button/link to switch to different languages to provide for this edge case. In addition, it is common practice not to offer every single language on your website. Many websites opt to feature the main language along with the other 'official languages' for the specific region or country that is being served. Also, date formats are different across different locales. 

## What are data- attributes good for?
Data attributes are useful in storing extra information that doesn't have any visual representation on standard HTML elements. Tying into JavaScript, data- attributes can be accessed via DOM manipulation by using `querySelector()` on the element and then accessing the `dataset` property. 

## Consider HTML5 as an open web platform. What are the building blocks of HTML5?
The building blocks of HTML5 include:
- Semantics - `<nav>`, `<header>`, `<footer>`, etc. **MathML** for embedding mathematical formulae.
- Storage - pages can store data locally and operate offline in a more efficient manner. **WebStorage** allows us to utilize Local Storage and Session Storage 
- Performance - Speed/hardware optimization 
- Multimedia - `<audio>` and `<video>` elements embed and allow manipulation of media content. The **Camera API** allows the use of the computer's camera. **WebRTC** (Real Time Communication) allows video conferencing in browser without external apps/plugins. **Canvas API** and **SVG** images. 
- Performace - Greater speed optimization and hardware usage. Web Workers that run independently of other scripts without effecting the performance of the page itself. The user can continue their experience while the worker runs in the background. The **History API** which allows the manipulation of browser history.
**Drag and drop API**! **Pointer Lock API** allows locking the pointer into the content so games don't go crazy when the pointer reaches the game window limit. 
- Device Access - allowing the use of device cameras, touch events, geolocation, and the detection of device orientation
- Styling - **CSS3**! Background styling, borders, CSS Transitions/Animations, and last but not least, **flexbox**.

## Describe the difference between a cookie, sessionStorage and localStorage.
- **localStorage** is a JavaScript object stores data up to 10MB with no expiration date. It will not be deleted when the browser is closed.
- **sessionStorage** stores data for _one session only_ with all data being lost when the browser tab/window is closed. 
- **cookies** are small pieces of data sent by the server to the user's browser. The browser stores the cookie and sends it back to the server in later requests. Cookies are used to differentiate requests sent from different browsers. (Think keeping a user logged in). Since cookies are sent with every request, they can decrease performance, hence the implementation of local and session storage.
