# Write a  function  that takes  an array of characters  and reverses the letters  in place. 

Why  an array  of characters instead of a string?

The goal of this question is to practice manipulating strings  _in place_. Since we're modifying the input, we need a  **mutable  ↴** type like  an array, instead of  JavaScript's  _immutable_  strings.

### Breakdown

In general, an  in-place algorithm will require swapping elements.

### Solution

We swap the first and last characters, then the second and second-to-last characters, and so on until we reach the middle.

	  function reverse(arrayOfChars) {

	  let leftIndex = 0;
	  let rightIndex = arrayOfChars.length - 1;

	  while (leftIndex < rightIndex) {

	    // Swap characters
	    const temp = arrayOfChars[leftIndex];
	    arrayOfChars[leftIndex] = arrayOfChars[rightIndex];
	    arrayOfChars[rightIndex] = temp;

	    // Move towards middle
	    leftIndex++;
	    rightIndex--;
	  }
	}

CC#C++JavaJavaScriptObjective-CPHPPython 2.7Python 3.6RubySwift

### Complexity

O(n)O(n)  time and  O(1)O(1)  space.
