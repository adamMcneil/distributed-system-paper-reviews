# Verus: A Practical Foundation for Systems Verification
## Summary
This is basic a rust program that a rust program and verifies that the assert statements (condition added to function definition) guarantee the conditions are met when you run the function (think of something like TLA+).

There is a spectrum from Math to computers.
Programming languages like C are close to computers and functional programming languages are near math.
Rust is close to a functional programming language.
They use a SAT solver to determine if the program is correct.
The system is not complete but they tried to cover the topics that would be helpful for developers.
You would use annotations like requires and ensure to write pre and post-conditions.
These conditions are something called EPR (effectively propositional) logic to define the pre and post-conditions.
There is a problem when you deal with very low-level manipulations and abstracting out pre and post-condition verus accounts for this and address the issues.
There was not a lot of talk about distributed systems, but still a great paper.


## Pros
- It is built with Rust
- It seems like it would be very helpful to the developer to have the requirements right with the implementation.
It would help understand what a function does when you do not know what it does and tell you how it hands edge cases.

## Cons
- It requires you to write loop invariant (it is not some magical tool that tells you if your program is correct)
- The program is not compatible with all of Rust.
- This seems like it would be very hard to write the conditions for the functions.
- In the conclusion they propose it as a tool for other researchers to use.

## Further Developments
It would be good to research what a linear type system is.
One of the aims of the paper is to provide a tool for developers to use so just installing and using would be a good place to start.
They also say that they want to be a starting point for other research projects.

## Related Topics
A good video on the paper can be found here:
https://www.youtube.com/watch?v=7WtWA0TTBqg
- SMT (is a problem like SAT)
- Dafny
- Linear Dafny (linear type system for Dafny)
- TLA+
