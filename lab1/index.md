## Lab Report 1 - William Lin (A17402486)

2023/10/03 Tuesday 12:00 ~ 1:50  
Some commands we learned about today are git clone, cd, ls, cat, java, javac, pwd and also how to host a repository on github pages. 

---

> Command: cd

1. Using cd command with no argument return the user to the home directory. (pwd:willop/Desktop)
```
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
willop@Williams-MacBook-Pro Desktop % cd
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
```
I was in the desktop directory before I use the cd command. Since the home directory on my computer is /Users/willop, using the cd command with no argument change my current directory from Desktop to willop

The output is correct and as expected.

2. cd command navigate us to the directory we typed after the cd command. (pwd:willop)
```
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
willop@Williams-MacBook-Pro ~ % cd Desktop 
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
```

I was in the home directory before I use the cd command. Since cd command allow user to enter a existing directory, Desktop is a existing directory under home. So using cd Desktop change the current directory from home to Desktop.

The output is correct and as expected.

3. cd command doesn't work when file is the argument. The output shows an error. (pwd:photo)
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % cd DSC02230.jpg
cd: not a directory: DSC02230.jpg
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
```

I was in the photo directory before I use cd command on a file. cd command allow user to change or enter a directory but not on a file so it printed cd: not a directory: DSC02230.jpg.

The output shows error because cd command can not enter a file. 

---
> Command: ls

1. List out all the files in the current directory. (pwd:photo)
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % ls
2023.07.19 Mazu			2023.09.19 Bryan's Website
2023.08.16 Grandma		DSC02230.jpg
2023.09.13 Japan Tokyo
```

I was in the photo directory before I use ls command. Using the ls command list out all the files in the current directory. Which is what the ternimal printed out.

The output is correct and expected.

2. List out all the files in the directory passed in as an argument if existed. (pwd:Desktop)
```
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
willop@Williams-MacBook-Pro Desktop % ls photo 
2023.07.19 Mazu			2023.09.19 Bryan's Website
2023.08.16 Grandma		DSC02230.jpg
2023.09.13 Japan Tokyo
```

I was in the Desktop direcotry this time. Using the ls command with argument or other directory in this case printed all the files in that directory. It printed out the same files as the previous question.

The output is correct and expected.

3. It just print out the name of the file because there is no other file except the file itself. (pwd:photo)
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % ls DSC02230.jpg 
DSC02230.jpg
```

Since ls list out all the file in the argument if passed in. The only file in a non directory is just the file itself. So the argument itself is being printed.

The output is correct and expected.

---
> Command cat

1. Nothing happened becuase cat command read a file and print it, since we pass in no file, it print no file. (pwd:test)
```
willop@Williams-MacBook-Pro test % pwd
/Users/willop/Desktop/UCSD/2023 Fall/CSE15L/test
willop@Williams-MacBook-Pro test % cat
^C
```

ince cat is used to print the data in a file. Nothing is passed to cat command here, so it is not likely to print anything.

The output should be a error because it goes into infinite loop here and I have to manually exit the line. I think it happens because nothing is passed in so there is nothing to print. 

2. When a directory is passed in as an argument it print out whether it is a dirctory or not. (pwd:CSE15L)
```
willop@Williams-MacBook-Pro CSE15L % pwd
/Users/willop/Desktop/UCSD/2023 Fall/CSE15L
willop@Williams-MacBook-Pro CSE15L % cat test
cat: test: Is a directory
```

cat command doesn't really work when passed a directory to it because there is nothing to print out.

The output is an error showing that the argument passed in is a directory, or it could also be a correct output if the user just want to know whether the argument passed in is a file or directory. 

3. When a file is passed in as an argument it print out the content in the file. (pwd:test)
```
willop@Williams-MacBook-Pro test % pwd
/Users/willop/Desktop/UCSD/2023 Fall/CSE15L/test
willop@Williams-MacBook-Pro test % cat word1.txt 
Hello, my name is William.%   
```

When a file is passed in as an argument to the cat command, it printed the text in the file. 

The output is correct and expected as it print out the content in the file word1.txt
