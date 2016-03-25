---
layout: post
comments: True
title:  "SelectionSort"
date:   2015-12-05
categories: [hack reactor, software engineering, bootcamp, sorting algorithms]
---

SelectionSort sorts an array by iterating through it, comparing each element with the smallest element in the array and swapping their places. This sorting algorithm has a O(n^2) time complexity so it is ideal for handling small lists.For this particular example, I am going to use a helper function called indexOfMinimum. The indexOfMinimum function will take in a start index and will return the index of smallest element ‘FROM’ the start index.

Below is the implementation.

{% highlight javascript %}

function selectionSort(arr) {
 
var temp;
var smallestIndex;
    for (var i = 0; i < arr.length; i++) {
         smallestIndex = indexOfMinimum(i);
         temp = arr[i];
         arr[i] = arr[smallestIndex];
         arr[smallestIndex] = temp;
    }
    return arr;
}
 
function indexOfMinimum(startIndex) {
 
var minIndex = startIndex;
var minValue = arr[startIndex];
      for (var i = startIndex + 1; i < arr.length; i++) {
          if (arr[i] < minValue) {
             minIndex = i;
             minValue = arr[i];
           }
      }
      return minIndex;
}
{% endhighlight %}