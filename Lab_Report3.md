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

````
JUnit version 4.13.2
.....E
Time: 0.004
There was 1 failure:
1) testReversed1(ArrayTests)
arrays first differed at element [0]; expected:<5> but was:<0>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)
        at org.junit.Assert.assertArrayEquals(Assert.java:418)
        at org.junit.Assert.assertArrayEquals(Assert.java:429)
        at ArrayTests.testReversed1(ArrayTests.java:32)
        ... 30 trimmed
Caused by: java.lang.AssertionError: expected:<5> but was:<0>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at org.junit.internal.ExactComparisonCriteria.assertElementsEqual(ExactComparisonCriteria.java:8)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:76)
        ... 36 more
````
**FIXING THE BUG**

Before 

````
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return newArray;
  }
````

After 

````
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
````

This fix addresses the issue because we just have to interchange newArray and arr in the loop and return newArray. Otherwise, we would have lost values in the process of reassigning values to the same array 'arr'.

## Part 2

## Command using : `FIND`

**First option - using `find -iname(name)`**

1. First example for a folder

````
prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -in
ame "*t_lsc*"
./technical/government/About_LSC
````

2. Second example for a file

````

prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -iname "*0023*TxT"
./technical/plos/pmed.0020023.txt
./technical/plos/pmed.0010023.txt
./technical/biomed/gb-2002-3-5-research0023.txt
````

The -iname tool helps us find a file not knowing its full name. It is useful for when we forget the file name and we’re trying to find the file from among a large amount of files and directories.

**Second option - using `find -type(type)`**

1. First example for a folder

````
prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -ty
pe d
./technical
./technical/government
./technical/government/About_LSC
./technical/government/Env_Prot_Agen
./technical/government/Alcohol_Problems
./technical/government/Gen_Account_Office
./technical/government/Post_Rate_Comm
./technical/government/Media
./technical/plos
./technical/biomed
./technical/911report
````

2. Second example for a file

````
prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -ty
pe f -name "*go*"
./technical/government/Media/Oregon_Poor.txt
./technical/government/Media/Ginny_Kilgore.txt
````

The -type tool helps list out files of a specific type from the folder. It's useful when we don’t want  files other than regular files or directories while using the find command.

**Third option - using `find -maxdepth(depth)`**

1. First example for a folder

````
prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -ma
xdepth 1 -name "*os*"
./technical/plos
````

2. Second example for a file

````
prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -maxdepth 2 -name "*123*"
./technical/plos/pmed.0020123.txt
````
The -maxdepth tool helps limit the search scope. It's useful when we only want to look for a folder within a certain depth.

**Fourth option - using `find -ipath(path)`**

1. First example for a folder

````
prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -ipath "*About*" -type d
./technical/government/About_LSC
````

2. Second example for a file

````
prashamshah@Prashams-MacBook-Pro docsearch % find ./technical -ipath "*Media*" -iname "*cu*"
./technical/government/Media/Funding_cuts_force.txt
./technical/government/Media/Too_Crucial_to_Take_Cut.txt
./technical/government/Media/Avoids_Budget_Cut.txt
````
The -ipath tool helps search for files within a path string. It's useful when we want to look for files inside a certain directory but  can’t remember where is the directory located.
