# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

<hr>

The only input we have into this black-box system would be the elements we input `n`.

We could vary by length, range of values, spread of values, distribution of values, repetitions of the same input values, etc.

Theoretically we could then test the given output to ensure it is actually sorted, and most importantly its runtime for any given input.

The first thing I would do as a sanity check would be to generate some relatively large input array size (say 1 000 000), and run the algorithm over and over again many times. I think this would be a good thing to check first, because it would be a quick and easy way to ensure that the output is actually deterministic in the first place. If this first test doesn't show deterministic characterstics, then we can already debunk the claim of $O(n)$ runtime.

I would then start with inputting lists of varying lengths, and then analyze the growth rate of the time to spit out an output, with inputsize `n` plotted against time.

I would then move on to inputting lists that are already sorted to some extent. I would try inputting a 100% sorted list, then a 90%, then an 80%, etc...

I would then compare the generated graph of runtimes to theoretical runtime curves of linear, logarithmic, and quadratic curves.

If the algorithm actually runs in $O(n)$ time, the data should show a plot that has a roughly straight line with a constant slope.

There is no such thing however as a sorting algorithm that has a general average time complexity of $O(n)$ with completely unknown inputs (the degree to which the input is already sorted or not is not known).

The best average case with unknown inputs generally for efficient sorting is $O(nlog(n))$. So the original claim of this algorithm is dubious.

- Referenced https://www.geeksforgeeks.org/time-complexities-of-all-sorting-algorithms/ for looking at general sorting algorithm behaviors and runtimes.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
