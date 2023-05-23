# Speeding up Command Line Tasks

## STEP 3

Start the timer.

## STEP 4 - Login to ieng6

* Open terminal and type the command `ssh cs15lsp23__@ieng6.ucsd.edu` (replace __ with your course specific account)

!Image[login.png]

## STEP 5 - Clone the Fork

* Open the fork in your repository and copy the ssh link in github.
* Run `git clone` with the copied link.
* Press < Command V > to paste the copied link.
* Press < Enter > to clone this repository.

!Image[git.png]

## STEP 6 - Run Tests

* First, `cd` into the lab7 directory.
* Enter `bash test.sh` in order to run the files in this directory.
* As we can see below, 2 tests ran and 1 failed.

!Image[bash.png]

## STEP 7 - Fixing The Code

* Enter `vim ListExamples.java` to enter the file.
* Type `/index1` and press <Enter>
* Press <Shift+N>
* Press the 'right arrow key' five times.
* When cursor is on '1', press 'X'.
* Then press 'I'.
* Enter the letter '2'.
* Click on <esc>.
* Press `:wq` to exit the vim file.
  
!Image[vim.png]
  
## STEP 8 - Run The Tests

* Enter `vim ListExamples.java` again by pressing the 'up arrow' twice.
* Enter `bash test.sh` in order to run the files in this directory using the 'up arrow' twice.
* We can see that there are no errors this time.
  
!Image[fixed.png]
  
## STEP 9 - Committing And Pushing The Changes


  

