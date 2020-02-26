# Notes: Brian Holt Computer Science Workshop

These are my notes to the FrontEndMasters Course http://btholt.github.io/four-semesters-of-cs/

Recommended book (free), Cormens Intro to Algorithms: https://web.ist.utl.pt/~fabio.ferreira/material/asa/clrs.pdf

## Big O

A way we can analyse how efficient algorithms are.

Considers differences in runtime in orders of magnitude.

For 3x^2 + x + 1, the big O would be O(n^2). We don't care about the 3, co-efficients, that sort of thing. Not about 30ms or 60ms - it's about the 30ms vs. 3 seconds.

### Big O types

#### O(1)

Constant time - runtime not affected by number of inputs. Means there's no loops in your code.

#### O(n)

We go through all inputs in a loop for O(n). As number of inputs rise, so does runtime in a linear fashion. We assume worst scenario i.e. needle is the last element in our input:

```javascript
const find = (needle, haystack) = {
    for (int i=0; i<haystack.length; i++){
        if (hackstack[i] === needle) return true;
    }
}
```

#### O(n^2)

We have an outer loop, and then within each iteration we have an inner loop that iterates over everything again. This is O(n^2):

```javascript
const makeTuples = (input) = {
    var answers = [];
    for (var i = 0; i < input.length; i++) {
        for (var j = 0; j < input.length; j++) {
            answer.push(input[i], input[j]])
        }
    }
}
```

n^2 algorithms are rarely appropriate. Try to find a better way.

#### O(log n)

Ideal function where you code employs divide-and-conquer strategy - which most often is recursive. That is, as the input length increases, the increases in time as you increment the length of the input diminishes e.g. using merge and quick sort.

## Recursion

Recursion is when you define something in terms of itself.

Very useful but is expensive in terms of memory - adds many functions to the stack by recursing too far down and you can cause stack overflow (usually occurs due to infinite recursion).

Code ought to be written to be readable and maintainable, in addition for function. Recursion is often particularly readable versus many for loops, so may be a favourable option.

CHECKPOINT: Trying to understand recursion example here https://frontendmasters.com/courses/computer-sciengitce/recursion-example
