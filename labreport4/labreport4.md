# Lab Report 4 - Doing it All from the Command Line  (Week 7)
## Pratham Savla

### Replicate Steps 4 - 7 

Step 4:
```
ssh prchheda@ieng6-201.ucsd.edu
```
The reason I used `-201` is because I was initially having trouble with the `-203` server and the TA's recommended switching over.
![ssh image](image1.png)


Step 5:
`git clone git@github.com:prsavla/lab7.git` then `<enter>`
![git clone](image2.png) 

Step 6:
`bash test.sh` then `<enter>`
![test cases failing](image3.png)


Step 7:
`vim ListExamples.java` then `<enter>` 



Edit the code to fix the test
Here is the exact pattern of keystrokes after typing in VIM:
`43J` , then  `E`, then  `R`, then `2` , then `:wq` then `<enter>`
Let me explain how these steps work to fix the bug in ListExamples.
`43J` will move the cursor down to the 43rd line where the bug exits.
`E` will go to the end of the word so the cursor will be on the 1 in `index1`.
`R` will go into replace and when followed with `2` it will replace `1` with `2`.
`:wq` will save and quite the file. 

Step 8: Rerun the tests to see if they passes
`bash test.sh` then `<enter>` 
[all tests passing](image4.png)

Step 9: Commit and Push the Resulting Change to My Github Account
- Type `git add --all` then `<enter>` 
- Type `git commit -m "fixed bug in ListExamples.java`then `<enter>` 
- Type`git push` then `<enter>`

[git add](image5.png)
[git commit](image6.png)

Here's an explanation for these commands:
`git add --all` adds all of the edits and new files to the current commit
`git commit -m "fixed bug...` commits the changes that you made to your local repository with a required commit message
`git push` syncs your local repository with github. 







