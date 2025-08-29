### Questions :

1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**?
2. How do you **create and insert a new element into the DOM**?
3. What is **Event Bubbling** and how does it work?
4. What is **Event Delegation** in JavaScript? Why is it useful?
5. What is the difference between **preventDefault() and stopPropagation()** methods?

### Answers :

1. In JavaScript, if we want to select just one element that has a unique identifier, you use a method that targets the id. Since an id is supposed to be unique, it will always give back only one element. If you want to select multiple elements that share the same class, there is another method that returns all elements with that class. There is also a more flexible method that lets you use any CSS-style selector, like a class, an id, or even combinations like a paragraph inside a division. This flexible method can either return just the first matching element or all matching elements as a list, depending on which version you use.

2. To create a new element in JavaScript, we use the document.createElement() function. Once the element is created, we can set its content or attributes. To place it on the page, we insert it into an existing element using .appendChild() or .append(). For example, if we make a new div and set its text to “Hello!”, we can then attach it to the body of the page, and it will appear there.

3. Event bubbling means that when something happens to a child element, like clicking a button, the event doesn’t just stay there. It also travels upward to the parent elements, and then to their parents, until it reaches the top of the document. For example, if you click a button inside a div, the button’s event will trigger first, then the div’s event, and then the body’s. It’s called “bubbling” because the event rises up step by step, just like bubbles rise to the surface of water.

4. Event delegation is a way to manage events more efficiently. Instead of adding an event listener to every single child element, you just put one event listener on the parent. Inside that listener, you check which child element actually triggered the event. This is very useful because it saves you from adding hundreds of listeners, and it also works for elements that are added later, after the page has already loaded. For example, if you add a click listener to a ul, you don’t need to attach one to each li—the parent can handle all the child clicks.

5. The preventDefault() method is used when you don’t want the browser to carry out its normal action. For example, clicking on a link usually takes you to another page, but if you call preventDefault(), the link won’t open. On the other hand, stopPropagation() is used to stop the event from moving up through the parent elements. For instance, if a button is inside a div, clicking the button would normally trigger both the button’s and the div’s events. But if you use stopPropagation(), only the button’s event will fire.
