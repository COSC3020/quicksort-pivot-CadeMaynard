[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12432223&assignment_repo_type=AssignmentRepo)
# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

## Probability Comparison
Referring to the slide on quick-sort that suggested we have a $\frac{1}{2}$ of the array is good pivots and $\frac{1}{4}$ on the front of the array and $\frac{1}{4}$ on the back contain bad pivots. We can evaluate the probability of getting a good pivot by checking all the collections of three that we might take from the array with a median in our "Good pivot range". This means this collection of three must either contain 2 good pivots or a good pivot, a bad pivot on the high end, and a bad pivot on the low end.
<br>
$\frac{1}{4}$ chance of a pivot that is too small so we will denote this possibility as $L$
<br>
$\frac{1}{4}$ chance of a pivot that is too large so we will denote this possibility as $R$
<br>
$\frac{1}{2}$ chance of a good pivot so we will see this possibility as $M$
<br>
Our combinations of three will look something like this: $(L,M,R)$ or some combination of those following the restrictions set above.
We calculate the individual probabilities of each combination as a product of the fractions each piece represents. Then we add all of those together to get the final fraction $\frac{11}{16}$ or the percentage $68.75$%

<br>
Sources:
Clayton helped me out with this
