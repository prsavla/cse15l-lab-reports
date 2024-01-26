# Lab Report 1 - Remote Access and FileSystem (Week 1)
## Pratham Savla

## Example #1: `cd` with no arguments
```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ 
```

Not an error | The command `cd` stands for change directory and it is used to change the current working directory. In this example, the current working directory is `/home/lecture1` and when `cd` is used with no command line arguments, you are taken back to the home directory from wherever you are by default.

## Example #2: `cd` with a path to a directory
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
Not an error | When you use `cd` with a path to directory, you are entering the directory. In this case, the current working directory is `/home` and using `cd` with a path to `lecture1` changes the current working directory to `/home/lecture1`. Note that in this case, `lecture1` has to be a sub directory of the home directory for this to work. 

## Example #3: `cd` with a path to a file 
```
[user@sahara ~/lecture1/messages]$ cd hi.txt
bash: cd: hi.txt: Not a directory
[user@sahara ~/lecture1/messages]$
```
Error | Using `cd` with a path to a file will give an error message because `cd` is only meant to be used only when working with directories or changing from parent to subdirectories. It does not work with files! Note that in this example, the current working directory was `/home/lecture1/messages`.

## Example #4: `ls` with no arguments
```
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$
```
Not an error |`ls` stands for list and when used with no arguments, it lists all the files in the current working directory. In this case, the current working directory is `/home`. 

## Example #5: `ls` with a path to a directory
```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
[user@sahara ~]$ 
```
Not an error | In this example, the working directory is `/home`. When using `ls` with a path to a directory, it will list all the files in the directory. Note that for `ls lecture1` to work, the current working directory cannot be `/home/lecture1`, otherwise an error message is thrown.

## Example #6: `ls` with a path to a file
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
[user@sahara ~/lecture1]$
```
Not an error | The current working directory is `/home/lecture1`. When using `ls` with a path to a file, it will simply display the file name. Note that Hello.java has to be a file inside `lecture1` for this to work. 

## Example #7: `cat` with no arguments
```
[user@sahara ~]$ cat
hello test message
hello test message
what does cat do?
what does cat do?
^C
[user@sahara ~]$
```
Not an error | The `cat` command stands for concactenate and it used to read the contents of a file without opening the file. However, when no command line arguments are specified, the `cat` command just reads from the terminal input and displays it into terminal output. When typing in `hello test message` as terminal input, `cat` will just display the same input as output. You have to use `^C` to break out of the task. The current working directory in this case is the home directory.

## Example #8: `cat` with a path to a directory
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$
```
Error | Because the `cat ` command is used to list the contents of a file, an error message is thrown when using it as a path to a directory. `cat` only works with files and the terminal outputs that lecture1 is a directory. In this case, the current working directory is also the home directory.

## Example #9: `cat` with a path to a file
```
[user@sahara ~/lecture1]$ cat Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}[user@sahara ~/lecture1]$
```
| Not an error | When using `cat` with a path to a file, it will read out the whole file as output without having to open it. Here, the conents of the Hello.java program are displayed and the current working directory is `lecture1`.

