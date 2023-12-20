# Augury Docs

Our attempt to document all the different systems that make up Augury

## How I write systems
Below is how I usually structure systems when designing and implementing them.

## Naming conventions
- Each function/global variable related to the system needs to be pre fixed with a shortened form of th system's name. For instance everything in the Tome library is prefixed with `tome`. keeping with consistent is important.
- There is always a separation between private and public functions/variables. Private functions/variables are always prefixed with `__` , so it Tome public functions/variables are prefixed with `tome` and private ones with `__tome`.
- Use explicit naming so future you can better understand the code.

## Best practices
- I try to keep a system as global as possible, writing functions in scripts and only using objects when necessary. For example Tome's controller object is dynamically created and then destroyed when no longer needed.
- Try to not repeat yourself. If you find yourself copying and pasting code, make that code into a helper/sub function. this will help with maintainability and save yourself headaches in the long run.
- Keep the user-facing API as simple as possible, only exposing functions and variables that are needed, keeping all system data prefixed with `__`
- practice encapsulation, but using getters and setters for classes. never edit class variables directly and when returning data from a class, return a copy of the data as to now expose editable system data to the end user.
