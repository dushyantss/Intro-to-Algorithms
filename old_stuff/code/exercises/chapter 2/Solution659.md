#This is fun
###Give an O.n lg k/-time algorithm to merge k sorted lists into one sorted list, where n is the total number of elements in all the input lists. (Hint: Use a minheap for k-way merging.)

##Solution
We take one element of each list and put it in a min-heap. Along with each element we have to track which list we took it from. When merging, we take the minimum element from the heap and insert another element off the list it came from (unless the list is empty). We continue until we empty the heap.

We have n steps and at each step we're doing an insertion into the heap, which is lg(k).