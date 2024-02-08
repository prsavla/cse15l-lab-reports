# Lab Report 3 - Bugs and Commands (Week 5)
## Pratham Savla

The bug I will be choosing from week 4's lab is in the ArrayExamples class and specifically the reversed method.
This is the original code with the bug:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
Here is a failure inducing input for the 
