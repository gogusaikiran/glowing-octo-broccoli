Event Loop in JavaScript – Learning Notes

Today I learned how the JavaScript Event Loop actually works behind the scenes.
At first, I thought JavaScript runs everything line by line, but now I understand that it uses a smart system to manage different types of tasks.

JavaScript is single-threaded, so it runs one thing at a time on the Call Stack.
But functions like setTimeout, fetch, or DOM events don’t run directly in the stack.
These go to Web APIs, which handle them separately.

When those tasks finish, their callbacks move into the Callback Queue.
At the same time, Promises and async operations go into a different place called the Microtask Queue.

The Event Loop keeps checking:

“Is the Call Stack empty?”

If yes → it first takes tasks from the Microtask Queue and runs them.

After microtasks, it moves to the Callback Queue.

This is why Promises run before timeouts, even if a timeout is written earlier in the code.

Overall, the Event Loop helps JavaScript look fast and responsive even though it's single-threaded.
This concept made more sense after watching the visualization in the video.
