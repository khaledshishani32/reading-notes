# Pain and Suffering

---

### It is not possible to reach your goal of success without fatigue or suffering, and this suffering refines your experience and turns from pain to a high value. You may feel fatigued, suffering, bad feelings, etc., but do not forget that, in return, it increases your skill capabilities in the field you learn, such as software development, after All, fatigue and suffering with determination you can reach the success you want.
---
# Beginners Guide to Big O
----
## What is the Big O Notation?
### Big O Notation is the language we use to describe the complexity of an algorithm. In other words, Big O Notation is the language we use for talking about how long an algorithm takes to run. It is how we compare the efficiency of different approaches to a problem. With Big O Notation we express the runtime in terms of — how quickly it grows relative to the input, as the input gets larger.
- how quickly the runtime grows — Being that it is difficult to determine the exact runtime of an algorithm. It depends on the speed of the computer processor. So instead of talking about the runtime directly, we use Big O Notation to talk about how quickly the runtime grows.
- relative to the input — If we were measuring our runtime directly, we could express our speed in seconds and minutes. Since we are measuring how quickly our runtime grows, we need to express our speed in terms of something else. With Big O Notation, we use the size of the input, which we call “n”. So we can say things like the runtime grows “on the order of the size of the input” (O(n)) or “on the order of the square of the size of the input” (O(n²)).
- as the input gets larger — Our algorithm may have steps that seem expensive when n is small but are eclipsed eventually by other steps as n gets larger. For Big O Notation analysis, we care more about the stuff that grows fastest as the input grows, because everything else is quickly eclipsed as n gets very large.
 


---
### Some Examples of Big O Notation
![](https://miro.medium.com/max/875/1*K1Z9e_ft1QtZk85VFPOIjA.png)

### This function runs in O(1) time (or “constant time”) relative to its input. This means that the input array could be 1 item or 1,000 items, but this function would still just require one “step.”

---
![](https://miro.medium.com/max/875/1*MRUrGb-zYPIkpARqOTY3yA.png)

### This function runs in O(n) time (or “linear time”), where n is the number of items in the array. This means that if the array has 10 items, I have to print 10 times. If it has 1,000 items, I have to print 1,000 times.

---

## Worst Case Scenario:
### When it comes to the Big O Notation, we are usually talking about the worst case scenario. At times the worst case runtime is significantly worse than the best case runtime.
![](https://miro.medium.com/max/1400/1*xD3TSO7439Tw3kWNNWiSaw.png)

### In this example, I might have 100 items in the haystack, but the first item might be the needle, in which case I would return in just 1 iteration of the loop. I can say this is O(n) runtime and the worst case scenario would be implied. But to be more specific I could say this is worst case O(n) and best case O(1) runtime.

 


---
### references :
---
[medium](https://medium.com)
[Google](https://www.google.com)
