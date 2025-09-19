# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary

Summarize your learnings from the lab here.

## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?

They are able to go across edges because we used gray coding when creating the KMap. Gray coding ensures that only one bit is changed when traveling between adjacent cells, even across edges. Topologically, it is equivalent to a torus.

### Why are the names Sum of Products and Product of Sums?

A "Sum of Products" is named that because that's exactly what it is. In boolean algebra, addition is equivalent to an OR gate, and multiplication is equivalent to an AND gate. As such, a Sum of Products is essentially ANDing together multiple OR equations. A Product of Sums is the opposite: ORing together multiple AND equations.

### Open the test.v file – how are we able to check that the signals match using XOR?

If you look at the truth table of an XOR gate, you'll notice that it outputs 0 only if the two inputs are equal: if they're both 0 or both 1. As such, you can use it as a makeshift equality operator.