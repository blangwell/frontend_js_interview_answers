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
It is important to make sure that you allow the user to visualize where to change the language of the page. Say you are an English speaker traveling abroad in China. You access a site that is rendered in Chinese. Best practices would be to have a clear button/link to switch to different languages to provide for this edge case.  
