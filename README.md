Answering the following questions:

1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
Ans: getElementById selects a single element by its unique ID and returns one element. getElementsByClassName selects all elements with a specific class and returns a live HTMLCollection. querySelector returns the first element matching any CSS selector, while querySelectorAll returns a static NodeList of all matching elements.

2. How do you create and insert a new element into the DOM?
Ans: To create and insert a new element into the DOM using JavaScript, you follow three main steps:
Create the element using document.createElement().Customize it by setting its attributes, text, or inner HTML.Insert it into the DOM using methods like appendChild(), prepend(), or insertBefore().

3. What is Event Bubbling and how does it work?
Ans: Event bubbling is a concept in the DOM event system where an event triggered on a nested element first runs its handler, then "bubbles up" to its parent elements, triggering their handlers in turn. For example, if you click a button inside a <div>, the click event first fires on the button, then on the <div>, and continues upward through the DOM tree until it reaches the root (document). This allows parent elements to respond to events from their children without needing to attach listeners to every child individually. You can control bubbling using event.stopPropagation() to prevent the event from moving up the tree. It's a powerful mechanism for efficient event handling and delegation.

4. What is Event Delegation in JavaScript? Why is it useful?
Ans: Event delegation is a technique in JavaScript where you attach a single event listener to a parent element to handle events triggered by its child elements. Instead of adding individual listeners to each child, the parent listens for events that bubble up from the children. This works because of event bubbling, where events move from the target element up through its ancestors.

It’s useful because it improves performance—especially when dealing with many dynamic elements—and simplifies code maintenance. For example, if you have a list where items are added or removed frequently, you can delegate click events to the list container rather than updating listeners every time the list changes. This makes your code cleaner, faster, and more flexible.

5. What is the difference between preventDefault() and stopPropagation() methods?
Ans: The difference between preventDefault() and stopPropagation() lies in what part of the event behavior they control.
preventDefault() stops the browser’s default action for an event. For example, it prevents a link from navigating or a form from submitting when the user clicks a button.
stopPropagation() stops the event from bubbling up to parent elements. It ensures that only the target element’s event handler runs, and the event doesn’t trigger handlers on ancestors.
