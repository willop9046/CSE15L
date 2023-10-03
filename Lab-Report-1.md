## Lab Report 1
by William Lin

> Command: cd

1. Nothing happened when the command cd is used with no arguments
```
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
willop@Williams-MacBook-Pro ~ % cd
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
```
2. cd command navigate us to the directory we typed after the cd command
```
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
willop@Williams-MacBook-Pro ~ % cd Desktop 
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
```
3. cd command doesn't work when file is the argument. The output shows an error.
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % cd DSC02230.jpg
cd: not a directory: DSC02230.jpg
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
```

> Command: ls

1. List out all the files in the current directory
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % ls
2023.07.19 Mazu			2023.09.19 Bryan's Website
2023.08.16 Grandma		DSC02230.jpg
2023.09.13 Japan Tokyo
```
2. List out all the files in the directory passed in as an argument if existed
```
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
willop@Williams-MacBook-Pro Desktop % ls photo 
2023.07.19 Mazu			2023.09.19 Bryan's Website
2023.08.16 Grandma		DSC02230.jpg
2023.09.13 Japan Tokyo
```
3. It just print out the name of the file because there is no other file except the file itself
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % ls DSC02230.jpg 
DSC02230.jpg
```


> Command cat

1. Nothing happened when the command cd is used with no arguments
```
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
willop@Williams-MacBook-Pro ~ % cd
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
```
2. cd command navigate us to the directory we typed after the cd command
```
willop@Williams-MacBook-Pro ~ % pwd
/Users/willop
willop@Williams-MacBook-Pro ~ % cd Desktop 
willop@Williams-MacBook-Pro Desktop % pwd
/Users/willop/Desktop
```
3. cd command doesn't work when file is the argument. The output shows an error.
```
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
willop@Williams-MacBook-Pro photo % cd DSC02230.jpg
cd: not a directory: DSC02230.jpg
willop@Williams-MacBook-Pro photo % pwd
/Users/willop/Desktop/photo
```
