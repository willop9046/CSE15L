## Lab Report 1
William Lin A17402486

2023/10/03 Tuesday 12:00 ~ 1:50  
Some commands we learned about today are git clone, cd, ls, cat, java, javac, pwd and also how to host a repository on github pages. 

---

> Command: cd

1. Nothing happened when the command cd is used with no arguments. (pwd:willop)
```
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
willop@Williams-MacBook-Pro ~ % cd
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
```
2. cd command navigate us to the directory we typed after the cd command. (pwd:willop)
```
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
willop@Williams-MacBook-Pro ~ % cd Desktop 
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
```
3. cd command doesn't work when file is the argument. The output shows an error. (pwd:photo)
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % cd DSC02230.jpg
cd: not a directory: DSC02230.jpg
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
```

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
2. List out all the files in the directory passed in as an argument if existed. (pwd:Desktop)
```
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
willop@Williams-MacBook-Pro Desktop % ls photo 
2023.07.19 Mazu			2023.09.19 Bryan's Website
2023.08.16 Grandma		DSC02230.jpg
2023.09.13 Japan Tokyo
```
3. It just print out the name of the file because there is no other file except the file itself. (pwd:photo)
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % ls DSC02230.jpg 
DSC02230.jpg
```

---
> Command cat

1. Nothing happened becuase cat command read a file and print it, since we pass in no file, it print no file. (pwd:test)
```
willop@Williams-MacBook-Pro test % pwd
/Users/willop/Desktop/UCSD/2023 Fall/CSE15L/test
willop@Williams-MacBook-Pro test % cat
^C
```
2. When a directory is passed in as an argument it print out whether it is a dirctory or not. (pwd:CSE15L)
```
willop@Williams-MacBook-Pro CSE15L % pwd
/Users/willop/Desktop/UCSD/2023 Fall/CSE15L
willop@Williams-MacBook-Pro CSE15L % cat test
cat: test: Is a directory
```
3. When a file is passed in as an argument it print out the content in the file. (pwd:test)
```
willop@Williams-MacBook-Pro test % pwd
/Users/willop/Desktop/UCSD/2023 Fall/CSE15L/test
willop@Williams-MacBook-Pro test % cat word1.txt 
Hello, my name is William.%   
```
