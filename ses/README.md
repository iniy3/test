# Search Engine Selector Documentation

## Overview
The "Search Engine Selector" website allows users to perform searches using different search engines. This documentation focuses on how to add more search engines to the existing code.

## Adding a New Search Engine
To add a new search engine, follow these steps:

1. **HTML Modifications:**
   - Locate the `.link-container` div in the HTML.
   - Add a new button or anchor (`<button>` or `<a>`) for the new search engine. Example:
     ```html
     <button onclick="search('newEngine')">
       <img src="path/to/newEngineIcon.svg" alt="New Engine"> New Engine </button>
     ```
     - Ensure to replace `newEngine` with a unique identifier for the engine and update the icon path accordingly.

2. **JavaScript Function:**
   - Add a new case in the `search` function in the script section. Example:
     ```javascript
     case 'newEngine':
       searchUrl = `//newengine.com/search?q=${searchQuery}`;
       break;
     ```
     - Replace `newEngine` with the same identifier used in the HTML.

3. **Testing:**
   - Test the new search engine button to ensure it opens the correct search results page.

## Notes
- Ensure that the search engine's URL is correctly formatted in the `search` function.
- Icons for new search engines should be hosted and accessible via a URL. Update the icon path accordingly.
- Maintain a consistent naming convention for the identifier used in HTML and JavaScript.

## Example
Suppose you want to add a "Reddit Search" engine:

**HTML:**
```html
<button onclick="search('reddit')">
  <img src="path/to/redditIcon.svg" alt="Reddit"> Reddit </button>
```

**JavaScript:**
```javascript
case 'reddit':
  searchUrl = `//www.reddit.com/search?q=${searchQuery}`;
  break;
```

Remember to replace placeholder values with actual details for the new search engine.

Feel free to repeat these steps to add more search engines as needed.
