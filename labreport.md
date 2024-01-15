# Lab Report 1 - Remote Access and FileSystem (Week 1)

## Example #1: cd with no arguments
```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ 
```

The command `cd` stands for change directory and it is used to change the current working directory. However, in this example, when no command line arguments are specified, `cd` takes you to the home directory. 

## Example #2: `cd` with a path to a directory
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```

## Example #3: `cd` with a path to a file 
```
[user@sahara ~/lecture1/messages]$ cd hi.txt
bash: cd: hi.txt: Not a directory
[user@sahara ~/lecture1/messages]$
```

## Example #4: `ls` with no arguments
```
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$
```

## Example #5: `ls` with a path to a directory
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
[user@sahara ~/lecture1]$
```

## Example #6: `ls` with a path to a file
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
[user@sahara ~/lecture1]$
```

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

## Example #8: `cat` with a path to a directory
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$
```

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

