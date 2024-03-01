# Text Fragment URL Generator Bookmarklet

This repository hosts a JavaScript Bookmarklet that enables users to generate URLs with Scroll-to-Text Fragment directly from their browser. By selecting text on a webpage and clicking the bookmarklet, users can create a link that, when visited, scrolls directly to the selected text on the page.

## How to Use

1. Create a new bookmark in your browser.
2. Copy and paste the JavaScript code provided below into the URL section of the bookmark.
3. When browsing, select text on a webpage that you wish to link directly to.
4. Click the bookmarklet to generate a URL with the selected text as a Scroll-to-Text Fragment.
5. A prompt will appear with the generated URL. Copy and use it as needed.

## Bookmarklet Code

```javascript
javascript:(function(){var text=window.getSelection().toString();if(text){var baseUrl=window.location.href.split('#')[0];var formattedText=text.trim().replace(/ /g,'%20');var newUrl=baseUrl+'#:~:text='+formattedText;prompt('Copy this URL:',newUrl);}else{alert('Please select some text on the page.');}})();
```

## Compatibility

This bookmarklet relies on the Scroll-to-Text Fragment feature, which may not be supported by all browsers. For detailed compatibility information, please refer to CanIUse: [URL Scroll-to-Text Fragment](https://caniuse.com/url-scroll-to-text-fragment).

## License

This project is released under the MIT License. See the LICENSE file for more details.

