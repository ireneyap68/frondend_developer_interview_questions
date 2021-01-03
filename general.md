### What is Big O notation, and why is it useful?
Big O notation is a convenient way to describe how fast a function is growing. When we compute the time complexity T(n) of an algorithm we rarely get an exact result, just an estimate. That’s fine, in computer science we are typically only interested in how fast T(n) is growing as a function of the input size n.

For example, if an algorithm increments each number in a list of length n, we might say: “This algorithm runs in O(n) time and performs O(1) work for each element”.

### What is the DOM?
The Document Object Model, or the “DOM”, is an interface to web pages. It is essentially an API to the page, allowing programs to read and manipulate the page’s content, structure, and styles. With the Document Object Model, programmers can create and build documents, navigate their structure, and add, modify, or delete elements and content. Anything found in an HTML or XML document can be accessed, changed, deleted, or added using the Document Object Model, with a few exceptions - in particular, the DOM interfaces for the internal subset and external subset have not yet been specified.

### What is the event loop?
The event loop is a programming construct or design pattern that waits for and dispatches events or messages in a program. The event loop works by making a request to some internal or external "event provider" (that generally blocks the request until an event has arrived), then calls the relevant event handler ("dispatches the event"). The event loop is also sometimes referred to as the message dispatcher, message loop, message pump, or run loop.
The event-loop may be used in conjunction with a reactor, if the event provider follows the file interface, which can be selected or 'polled' (the Unix system call, not actual polling). The event loop almost always operates asynchronously with the message originator.
When the event loop forms the central control flow construct of a program, as it often does, it may be termed the main loop or main event loop. This title is appropriate, because such an event loop is at the highest level of control within the program.


### What is a closure?
The most simple way to think of a closure is a function that can be stored as a variable (referred to as a "first-class function"), that has a special ability to access other variables local to the scope it was created in.

Example (JavaScript):

    var setKeyPress = function(callback) {
        document.onkeypress = callback;
    };

    var initialize = function() {
        var black = false;

        document.onclick = function() {
            black = !black;
            document.body.style.backgroundColor = black ? "#000000" : "transparent";
        }

        var displayValOfBlack = function() {
            alert(black);
        }

        setKeyPress(displayValOfBlack);
    };

initialize();
The functions1 assigned to document.onclick and displayValOfBlack are closures. You can see that they both reference the boolean variable black, but that variable is assigned outside the function. Because black is local to the scope where the function was defined, the pointer to this variable is preserved.

If you put this in an HTML page:

Click to change to black
Hit [enter] to see "true"
Click again, changes back to white
Hit [enter] to see "false"
This demonstrates that both have access to the same black, and can be used to store state without any wrapper object.

The call to setKeyPress is to demonstrate how a function can be passed just like any variable. The scope preserved in the closure is still the one where the function was defined.

Closures are commonly used as event handlers, especially in JavaScript and ActionScript. Good use of closures will help you implicitly bind variables to event handlers without having to create an object wrapper. However, careless use will lead to memory leaks (such as when an unused but preserved event handler is the only thing to hold on to large objects in memory, especially DOM objects, preventing garbage collection).


### How does prototypal inheritance work, and how is it different from classical inheritance? (this is not a useful question IMO, but a lot of people like to ask it)

### How does this work?

### What is event bubbling and how does it work? (this is also a bad question IMO, but a lot of people like to ask it too)

### Describe a few ways to communicate between a server and a client. Describe how a few network protocols work at a high level (IP, TCP, HTTP/S/2, UDP, RTC, DNS, etc.)

### What is REST, and why do people use it?
REST is an architectural style that uses simple HTTP calls for inter-machine communication instead of more complex options like CORBA, COM+, RPC, or even SOAP. Using REST means your calls will be message-based and reliant on the HTTP standard to describe these messages. It works because you're not tying your API to your client-side technology. You could imagine that this API is accessible from a client-side Web project, an iOS app, an IoT device and even a Windows Phone. This allows you to build the infrastructure for your organization with fewer worries about the longer-term marrying to a particular client-side stack. The server lives longer than the client. It always does.


### My website is slow. Walk me through diagnosing and fixing it. What are some performance optimizations people use, and when should they be used?
https://www.altexsoft.com/blog/engineering/12-techniques-of-website-speed-optimization-performance-testing-and-improvement-practices/


### What frameworks have you used? What are the pros and cons of each? Why do people use frameworks? What kinds of problems do frameworks solve?


# General Questions
1. What did you learn yesterday/this week?
- Cooperative learning which is combination of the two folks, peer-to-peer instruction. I learned to work together(interaction and communication) and solve problem with each other.  

2. What excites or interests you about coding?
- I love programming because of it's endless applications, my wish for something and programming can made it possible if I have enough resources and skill, second thing I love about programming is that, it build my problem solving skill which increases my creativity, and when I become more creative for a thing, I explore it, I love it, and I dream about it.

3. What is a recent technical challenge you experienced and how did you solve it?
- I wish it were more exciting, but, I’m dealing with moving a large Mongo database from my local machine to a remote server. I had to learn how to make backups and how to restore. I also had to deal with timeout issues. Finally, my peers guided me!

4. When building a new web site or maintaining one, can you explain some techniques you have used to increase performance? 
- Reduce external HTTP requests
    - In many cases, a large portion of a website's load time comes from external HTTP requests. The speed at which an external resource loads can vary depending on the hosting provider's server infrastructure, location, etc. Your first goal when reducing external HTTP requests should be to examine your website with a minimalist outlook. Study each component of your webpages, and eliminate any features that do not improve the experience of your visitors. These features may be:
        1. Unnecessary images
        2. Unnecessary JavaScript
        3. Excessive CSS
        4. Unnecessary plugins

5. Can you describe some SEO best practices or techniques you have used lately?
-  Highlight data with Google Webmaster Tools. Data highlighter allows us to highlight parts of our website through Google Webmaster Tools, without having to make any code changes. That will help us display ratings, prices, reviews along with our rich snippet in organic results. Even further, this will increase our chances of getting a Google knowledge card featuring our website. So if our website includes listings, reviews or events, here’s how to make the results show in Google

6. Can you explain any common techniques or recent issues solved in regards to front-end security?
- Front-end validation is important! In fact, there’s a lot of client-side attack vectors that you should worry about. In particular, two you should worry about are cross-site scripting (XSS) and malware in third party libraries you’re using.

- To give an example of how this is a client-side concern, consider the [Magecart malware](https://www.nbcnews.com/tech/tech-news/what-magecart-credit-card-stealing-malware-proves-hard-stop-n948176). Major websites like Ticketmaster, Forbes, and British Airways have been affected when code they were relying on was modified to include credit card skimming Javascript. This malware monitored the page for credit card inputs, then sent the data back to its servers. Since it all happened entirely in the browser, no company internal firewall or server agent would have detected it.

7. What actions have you personally taken on recent projects to increase maintainability of your code?

8. Talk about your preferred development environment.

9. Which version control systems are you familiar with?

10. Can you describe your workflow when you create a web page?

11. If you have 5 different stylesheets, how would you best integrate them into the site?

12. Can you describe the difference between progressive enhancement and graceful degradation?

13. How would you optimize a website's assets/resources?

14. How many resources will a browser download from a given domain at a time?
- What are the exceptions?

15. Name 3 ways to decrease page load (perceived or actual load time).

16. If you jumped on a project and they used tabs and you used spaces, what would you do?

17. Describe how you would create a simple slideshow page.

18. If you could master one technology this year, what would it be?

19. Explain the importance of standards and standards bodies.

20. What is Flash of Unstyled Content? How do you avoid FOUC?

21. Explain what ARIA and screenreaders are, and how to make a website accessible.

22. Explain some of the pros and cons for CSS animations versus JavaScript animations.

23. What does CORS stand for and what issue does it address?

24. How did you handle a disagreement with your boss or your collaborator?

25. What resources do you use to learn about the latest in front end development and design?

26. What skills are needed to be a good front-end developer?

27. What role do you see yourself?

28. Explain the difference between cookies, session storage, and local storage?
