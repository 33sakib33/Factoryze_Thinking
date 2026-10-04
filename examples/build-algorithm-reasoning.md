# Build Algorithm Reasoning example

## Starting request

**User**

> Use `$build-algorithm-reasoning`. Write a fast function that merges overlapping intervals.

**Agent**

> I need the problem contract before implementation.
>
> 1. What exact input and output formats must the function use?
> 2. Does contact at one endpoint count as overlap?
> 3. What input size, time limit, memory limit, and mutation rule apply?

After the contract is clear, the agent asks for the learner's natural-language algorithm.

## Incorrect learner attempt

**User**

> Sort by start. When the next interval overlaps, replace the current end with the next end.

**Agent**

> For `[[1, 10], [2, 3]]`, this step changes `[1, 10]` to `[1, 3]`.
>
> The result loses part of the first interval.
>
> Revise only the overlap update. State the exact end value after every overlap.

The agent supplies a counterexample, but it does not supply the corrected update.

## Readiness evidence

Before implementation, the learner must explain:

- initialization and ordered steps;
- each important condition and state change;
- why the process stops;
- a rule that remains true during repeated steps;
- why the result is correct;
- how work and stored data grow with input size;
- risky cases and exact expected results;
- finish checks that reject an incomplete result.

Before one consequential test, the agent asks the learner to predict the exact result and explain why.
