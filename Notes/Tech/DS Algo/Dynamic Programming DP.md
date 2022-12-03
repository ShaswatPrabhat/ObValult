* The Problem can be broken down into [[overlapping subproblems]] with each subproblem being used multiple times
* [[Optimal substructure]] - Solution to main problem can be found by solving each optimal subproblem
* [[Greedy]] - has [[Optimal substructure]]  but no [[overlapping subproblems]]
* [[Divide and Conquer]] - can be divided into subproblems but these are not overlapping. Almost always these are independent
* [[Bottom-up]] - Tabulation way for [[Dynamic Programming DP]] , ususally faster [[runtime]] as it uses [[iteration]] instead of recursion
* [[Top-down]] - Memoization for [[Dynamic Programming DP]] , usually easier to write
* For [[Bottom-up]] start at base cases and then build to the solution
* For [[Top-down]] we calculate solution using [[recursion]] . This might make it too costly for [[overlapping subproblems]] so we memoize some data to make it more effecient
* The first characteristic that is common in DP problems is that the problem will ask for the optimum value (maximum or minimum) of something or the number of ways there are to do something
* Sometimes, a problem in this format (asking for the max/min/longest etc.) is meant to be solved with a [[Greedy]] algorithm
* The second characteristic that is common in DP problems is that **future "decisions" depend on earlier decisions**.
* When you're solving a problem on your own and trying to decide if the second characteristic is applicable, assume it isn't, then try to think of a counterexample that proves a greedy algorithm won't work. If you can think of an example where earlier decisions affect future decisions, then DP is applicable
* 