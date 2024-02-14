# Lab Report 3

## Part 1 

**The Code**

    
  ````
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return newArray;
  }

  ````

Failure-inducing Input (Test case)

````
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
````

Non Failure-inducing Input

````
@Test
  public void testReverseOneElement() {
    int[] input1 = {6};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{6}, input1);
  }
````

**SYMPTOMS**


## Part 2

