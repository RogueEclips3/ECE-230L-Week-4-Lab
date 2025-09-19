# Lab 04 - SOP/POS and KMaps

## Lab Summary

In this lab, we learned the basics of optimizing an equation using a KMap. We started with a truth table, then create a unoptimized Sum of Products. Then, using a KMap, we created an optimized SOP and an optimized POS by grouping 1s and 0s into groups of powers of 2. We then compared the optimized equations to the unoptimized SOP to confirm that they were equivalent. Finally, we programmed our equations onto a Basys3 FPGA board.

## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?

They are able to go across edges because we used gray coding when creating the KMap. Gray coding ensures that only one bit is changed when traveling between adjacent cells, even across edges. Topologically, it is equivalent to a torus.

### Why are the names Sum of Products and Product of Sums?

A "Sum of Products" is named that because that's exactly what it is. In boolean algebra, addition is equivalent to an OR gate, and multiplication is equivalent to an AND gate. As such, a Sum of Products is essentially ANDing together multiple OR equations. A Product of Sums is the opposite: ORing together multiple AND equations.

### Open the test.v file – how are we able to check that the signals match using XOR?

If you look at the truth table of an XOR gate, you'll notice that it outputs 0 only if the two inputs are equal: if they're both 0 or both 1. As such, you can use it as a makeshift equality operator.