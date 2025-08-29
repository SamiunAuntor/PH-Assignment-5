### Answer the following questions clearly:

1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**?
2. How do you **create and insert a new element into the DOM**?
3. What is **Event Bubbling** and how does it work?
4. What is **Event Delegation** in JavaScript? Why is it useful?
5. What is the difference between **preventDefault() and stopPropagation()** methods?

### Answer

1. In JavaScript, getElementById is used when you want to select just one element by its unique id. Since ids are supposed to be unique, it always gives back only one element. On the other hand, getElementsByClassName is used when you want to select multiple elements that share the same class name. This returns a collection of elements, not just one. The querySelector method is more flexible because you can pass in any CSS selector, like a class, an id, or even something like div p, but it only returns the first match. Finally, querySelectorAll works the same way but gives you all the elements that match the selector in the form of a list.

2. To create a new element in JavaScript, we use the document.createElement() function. Once the element is created, we can set its content or attributes. To place it on the page, we insert it into an existing element using .appendChild() or .append(). For example, if we make a new <div> and set its text to “Hello!”, we can then attach it to the body of the page, and it will appear there.

3. Event bubbling means that when something happens to a child element, like clicking a button, the event doesn’t just stay there. It also travels upward to the parent elements, and then to their parents, until it reaches the top of the document. For example, if you click a button inside a <div>, the button’s event will trigger first, then the <div>’s event, and then the body’s. It’s called “bubbling” because the event rises up step by step, just like bubbles rise to the surface of water.

4. Event delegation is a way to manage events more efficiently. Instead of adding an event listener to every single child element, you just put one event listener on the parent. Inside that listener, you check which child element actually triggered the event. This is very useful because it saves you from adding hundreds of listeners, and it also works for elements that are added later, after the page has already loaded. For example, if you add a click listener to a <ul>, you don’t need to attach one to each <li>—the parent can handle all the child clicks.

5. The preventDefault() method is used when you don’t want the browser to carry out its normal action. For example, clicking on a link usually takes you to another page, but if you call preventDefault(), the link won’t open. On the other hand, stopPropagation() is used to stop the event from moving up through the parent elements. For instance, if a button is inside a <div>, clicking the button would normally trigger both the button’s and the <div>’s events. But if you use stopPropagation(), only the button’s event will fire.