# Detecting Logic Bugs in Database Engines via Equivalent Expression Transformation
## Summary
This paper proposes a way to detect bugs that cause database engines to process data incorrectly.
They propose a novel and general approach called equivalent expression transformation.
At a very high level they modify queries to the database and the validating that the results before and after the modification are the same.
Pratically they modify a query so that it should produce the same output and the verify that the output is that same.
Two ideas that they introduce are determined boolean expression and redundant branch structure.
I think that these are the ways that they can query to find bugs.
They randomly pick one of the logic rules to apply to the query.

The paper is really about this group of students writing a general integration test suite for database companies.
One of the biggest pluses of the paper is that the system can work on an arbitrate query.
However, since the system tests the database itself and not the query this is not quite as useful.
The existing solution is a system called PQS that generates a query that should select specific rows.


## Pros
- Is tested on many applications that are used a lot in actual applications.
- Found 66 unquie bugs 35 of them being logic bugs.
It's pretty cool they report all of the bugs that they found to the database form and some of them get fixed.
- They can apply their bug detector to an arbitrary query.

## Cons
- I don't feel like they give a concert definition of a logic bug. They only say they produce wrong results.
- Only detects bugs with a boolean which I guess is what they mean by logic bugs.


