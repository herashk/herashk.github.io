---
layout: post
comments: True
title:  "bubbleSort"
date:   2015-12-18
categories: [hack reactor, software engineering, bootcamp, sorting algorithms]
---

BubbleSort is one of the most basic sorting algorithms. The algorithm sorts an array by starting from the first element, comparing it to the second. If the first element is greater than the second, their indexes are swapped. Then the second element is compared to the third and third is compared to the fourth and so on. At the end of the array, the algorithm starts from the beginning of the array again and repeats this entire process until the array is completely sorted. Because of having to repeat iterating through the array possibly multiple times, it is quite slow in speed, with time complexity of O(n^2) and is recommended for data set that has only few unsorted items. Below is implementation of bubbleSort in O(n^2) complexity.

{% highlight javascript %}
var bubbleSort = function(array){
  for(var j = 0; j < array.length; j++){
     for(var i = 0; i < array.length; i++){
       if(array[i] > array[i+1]){
         var bigger = array[i];
         array[i] = array[i+1];
         array[i+1] = bigger;
       }
     }
  }
  return array;
};
{% endhighlight %}

But during sorting, there could be instances where no elements are swapped because parts of the array are already sorted. Then, we do not have to iterate through the entire array. Below is a more optimized version of bubbleSort.

{% highlight javascript %}
var bubbleSort2 = function(array){
   for(var j = 0; j < array.length; j++){
     var swapped = false;
     for(var i = 0; i < array.length; i++){
        if(array[i] > array[i+1]){
           swapped = true;
           var bigger = array[i];
           array[i] = array[i+1];
           array[i+1] = bigger;
         }
      }
      if(!swapped){
         break;
      }
   }
   return array;
};
{% endhighlight %}

Finally, if you walk through every step of bubbleSort, you will see that we do not need to consider every element inside the array. I like to imagine bubbleSort as a pile of snow rolling downhill. As it rolls down, the pile gets bigger and bigger. As the array gets sorted, always the largest value ‘bubbles’ up to the end, so we do not have to consider the last item in the array. Below is the second optimized implementation.

{% highlight javascript %}
var bubbleSort3 = function(array){
   for(var j = 0; j < array.length; j++){
      var swapped = false;
      for(var i = 0; i < array.length-j; i++){
        if(array[i] > array[i+1]){
           swapped = true;
           var bigger = array[i];
           array[i] = array[i+1];
           array[i+1] = bigger;
        }
      }
      if(!swapped){
        break;
      }
   }
   return array;
};
{% endhighlight %}
