# _What is call stack in node JS?_
- is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions what function is currently being run and what functions are called from within that function
>- When a ***script*** calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
>> Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
>>> When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
>>>> If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

- **The JavaScript engine** (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
## Temporarily store: 
- When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.
