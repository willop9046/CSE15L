## Week 5 - Lab Report 3 - William Lin (A17402486)

2023/10/31 Tuesday 12:00 ~ 1:50  

> Part 1 - Bugs

A failure-inducing input
```
@Test
  public void testReversedNormal() {
    int[] input1 = { 1, 2, 3};
    assertArrayEquals(new int[]{ 3, 2, 1}, ArrayExamples.reversed(input1));
  }

Output:
1) testReversedNormal(ArrayTests)
arrays first differed at element [0]; expected:<3> but was:<0>
```
- There are bugs in the reversed method, so any array that isn't size 0 or 1 will result in a failure-inducing input. 

An input that doesn’t induce a failure
```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }

Output:
OK (2 tests)
```
- The above test doesn't result in test failure because the element position when array size are 0 or 1 won't change. 

The symptom, as the output of running the tests
![Image](symptom.png)

The bug, as the before-and-after code change required to fix it 
Before:
```
 static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

After:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
- The new code fix the issue because it copyed all the elements one by one to a new array newArray and return it. 

> Part 2 - Researching Commands - grep

- -c option 

Why Useful:
User knows the count of mathcing lines, keep track of the files that have matching names.

On Files:
```
willop@Williams-MacBook-Pro biomed % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical/biomed
willop@Williams-MacBook-Pro biomed % ls | grep -c "rr"
9
```
The command search through the directory "biomed" and count the files that have a filename that includes "rr"
Useful because user knows the count of mathcing lines, keep track of the files that have matching names.

On Directory:
```
willop@Williams-MacBook-Pro technical % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical
willop@Williams-MacBook-Pro technical % ls | grep -c "biomed"
1
```
The command search through the directory "technical" and count the directory that have a name that includes "biomed"
Useful because user knows the count of mathcing lines, keep track of the direcotries that have matching names.

- -v option 

Why Useful:
User knows the invert count of mathcing lines, keep track of the files that doesn't have a matching names.

On Files:
```
willop@Williams-MacBook-Pro biomed % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical/biomed
willop@Williams-MacBook-Pro biomed % ls | grep -c -v "rr"
828
```

The command count the files that don't have character "rr" in the filename.
Useful when user don't know what file to search for but know files he doesn't want to find.

On Directory:
```
willop@Williams-MacBook-Pro technical % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical
willop@Williams-MacBook-Pro technical % ls | grep -c -v "biomed"
3
```
The command count the directory that doesn't have the filename "biomed".
Useful when user don't know what directory to search for but know directory he doesn't want to find.

- -n option 

Why Useful:
User knows the precede of each matching line with a line number. So the user knows where the files are located relatively on top or near the end of the file.

On Files:
```
willop@Williams-MacBook-Pro biomed % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical/biomed
willop@Williams-MacBook-Pro biomed % ls | grep -n "rr"
829:rr166.txt
830:rr167.txt
831:rr171.txt
832:rr172.txt
833:rr191.txt
834:rr196.txt
835:rr37.txt
836:rr73.txt
837:rr74.txt
```

The command list the files that have the filename "rr" included in the directory have list them out with line number indicating where they are in the diretory
Useful because we can locate where the files are listed in the directory

On Directory:
```
willop@Williams-MacBook-Pro technical % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical
willop@Williams-MacBook-Pro technical % ls | grep -n "biomed"
2:biomed
```

The command list the directories that have the name "biomed" included in the directory have list them out with line number indicating where they are in the diretory
Useful because we can locate where the directories are listed in the directory

- -i option 

Why Useful:
User can ignore uppercase and lowercase issue when find files or directory

On Files:
```
willop@Williams-MacBook-Pro biomed % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical/biomed
willop@Williams-MacBook-Pro biomed % ls | grep -i -c "RR"
9
```

The command ignore the uppercase and lowercase when search through files
Useful when the user have filesname with upper and lower case and want to search files by name but don't know weather the filename have upper or lower case.

On Directory:
```
willop@Williams-MacBook-Pro technical % pwd
/Users/willop/Desktop/UCSD/CSE15L-FA23/docsearch/technical
willop@Williams-MacBook-Pro technical % ls | grep -i "Biomed"
biomed
```

The command ignore the uppercase and lowercase when search through directory
Useful when the user have directories with upper and lower case and want to search directory by name but don't know weather the directory have upper or lower case.

> Citation 
URL : https://en.wikibooks.org/wiki/Grep





