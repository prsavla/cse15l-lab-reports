# Lab Report 3 - Bugs and Commands (Week 5)
## Pratham Savla

The bug I will be choosing from week 4's lab is in the ArrayExamples class and specifically the reversed method.
This is the original code with the bug:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
Here is a failure inducing input for the method:
```
@Test
  public void testReversed1() {
    int[] input1 = {1,2,3,4,5};
    assertArrayEquals(new int[]{5,4,3,2,1},ArrayExamples.reversed(input1));
    }
```
Here is an input that does not induce a failure:
```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
    
  }
```
Here is the JUnit output (Symptom) of the failure-inducing test:
![Fail Test](fail-test.png)

The before code was shown earlier. Here is the after code that fixes the bug:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
## Explanation of the Bug: 
The main issue behind the `reversed()` method was that although `newArray` was being initialized, the wrong assignment operation was being done. The for-loop in the original code was assigning each value of `arr[i]`, the original array, with the reverse values of `newArray` instead of the other way around. Also, the wrong array was being returned. `newArray` should be initialized and assigned the reverse values of `arr`, and then finally, `newArray` should be returned. 

# Part 2 - Researching Commands
The command I will be choosing to research is the `find` command. 
1) The first interesting command line argument to use with file is -mtime which allows you to search for files based on their modification time.
   Here is the general scafollding: `find /path/to/search -mtime -7`. Will search for files modified within the last 7 days.

   I went ahead and modified one of the files in technical to get some output.
   
   





