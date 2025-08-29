### Questions :

1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**?
2. How do you **create and insert a new element into the DOM**?
3. What is **Event Bubbling** and how does it work?
4. What is **Event Delegation** in JavaScript? Why is it useful?
5. What is the difference between **preventDefault() and stopPropagation()** methods?

### Answers :

1. getElementById selects a single unique element, getElementsByClassName selects multiple elements with the same class, and querySelector/querySelectorAll use CSS selectors for flexible selection.

2. Create an element, set its content or attributes, and attach it to the DOM through a parent element.

3. An event on a child element travels upward to parent elements, triggering their events in order.

4. Add a single event listener to a parent to handle events from all its children efficiently, even for dynamically added elements.

5. preventDefault() stops the browser’s default action, while stopPropagation() stops the event from moving up to parent elements.
