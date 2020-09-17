# HTML Questions
1. What does a doctype do?
- A DOCTYPE is a required preamble. DOCTYPEs are required for legacy reasons. When omitted, browsers tend to use a different rendering mode that is incompatible with some specifications. Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.

2. How do you serve a page with content in multiple languages?
- Always use a language attribute on the html tag to declare the default language of the text in the page. When the page contains content in another language, add a language attribute to an element surrounding that content.

- Use the lang attribute for pages served as HTML, and the xml:lang attribute for pages served as XML. For XHTML 1.x and HTML5 polyglot documents, use both together.

- Use language tags from the IANA Language Subtag Registry. You can find subtags using the unofficial Language Subtag Lookup tool.

- Use nested elements to take care of content and attribute values on the same element that are in different languages.

3. What kind of things must you be wary of when designing or developing for multilingual sites?
- NO CULTURE AWARENESS. When two people from different cultures meet, they need to learn one another’s customs. In terms of design, this means adapting all the design elements to the needs of the target culture. But how not to offend someone from a different culture? Solution: The right answer to this question is to research. Find out what the customs of the country are and try to go with neutral principles. For example, in the west it is normal for people to use images of women in T-shirts and with hair flowing around; however, in the east, this may seem offensive since their women are protected from the eyes of foreigners. If you want to respect your target country’s customs, you will accept this and adjust your design accordingly. Similarly, color psychology and color theory also depend on culture and customs. In the west, it is normal for people to use blue for IT companies; on the other hand, in the east (e.g. in Korea or Mexico), blue is the color of mourning.

4. What are data- attributes good for?
- The data-* attribute is used to store custom data private to the page or application.The data-* attribute gives us the ability to embed custom data attributes on all HTML elements. The stored (custom) data can then be used in the page's JavaScript to create a more engaging user experience (without any Ajax calls or server-side database queries).

5. Consider HTML5 as an open web platform. What are the building blocks of HTML5?
- Semantics: allowing you to describe more precisely what your content is.
- Connectivity: allowing you to communicate with the server in new and innovative ways.
- Offline and storage: allowing webpages to store data on the client-side locally and operate offline more efficiently.
- Multimedia: making video and audio first-class citizens in the Open Web.
- 2D/3D graphics and effects: allowing a much more diverse range of presentation options.
- Performance and integration: providing greater speed optimization and better usage of computer hardware.
- Device access: allowing for the usage of various input and output devices.
- Styling: letting authors write more sophisticated themes.

6. Describe the difference between a cookie, sessionStorage and localStorage.
- In terms of capabilities, cookies only allow you to store strings. sessionStorage and localStorage allow you to store JavaScript primitives but not Objects or Arrays. Session storage will generally allow you to store any primitives or objects supported by your Server Side language/framework.

- localStorage and sessionStorage are relatively new APIs and are near identical (both in APIs and capabilities) with the sole exception of persistence. sessionStorage is only available for the duration of the browser session (and is deleted when the tab or window is closed) - it does however survive page reloads.

- localStorage and sessionStorage are perfect for persisting non-sensitive data needed within client scripts between pages, for example: preferences, scores in games.

- Cookies are used for authentication purposes and persistence of user data, all cookies valid for a page are sent from the browser to the server for every request to the same domain - this includes the original page request, any subsequent Ajax requests, all images, style-sheets, scripts and fonts.
