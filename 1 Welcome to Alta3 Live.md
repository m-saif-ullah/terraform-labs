### [Lab Objective](https://live.alta3.com/content/terraform/labs/content/welcome/welcome-w-vid.html#lab-objective)

These labs will guide you through **hands-on, step-by-step exercises**, with _detailed explanations for each step_.

The virtual environment you will use to perform these labs is available to you **24/7** throughout the duration of your course. _We do not turn them off in between sessions_.

#### [Getting Started](https://live.alta3.com/content/terraform/labs/content/welcome/welcome-w-vid.html#getting-started)

Let's make sure you are ready to start running through these labs.

Even so, you may have to use a new key-combination to use the copy-paste functionality. Let's practice it now.

If you click on the little clipboard icon in a lab, it will copy whatever text or code block is next to it, and will be available to paste into the virtual machine.

`student@bchd:~$` `# copy me!`

After clicking on the , you will then be able to paste the command or code block wherever you would like.

Typically, you will want to paste into the Virtual Machine's terminal.

Each browser is different, but there are several ways to do this:

1.  In the terminal, right click, then select `paste` (or) `paste as plain-text` (depending on the browser)
2.  Shift Insert
3.  Ctrl Shift v

Go ahead and try to paste the text of `# copy me!` into your terminal now.

#### [Fundamental Commands](https://live.alta3.com/content/terraform/labs/content/welcome/welcome-w-vid.html#fundamental-commands)

Not every person in this course has experience using a terminal to interact with a computer. This section is for those who may not have previous experience using a Linux terminal.

First of all, take a look at your command prompt to try to understand what it can teach us. It should look like:

`student@bchd:~$`

* **student** is the name of the user
* **bchd** is the hostname of the machine
* **~** (to the right of the colon) shows us the present working directory. Specifically, **~** refers to this user's home directory of `/home/student`.
* **$** shows us that this is a typical user (vs. **#** would indicate that it is the **root** user)

Now let's run some fundamental commands to get to know our environment a little bit better. Remember, we are starting in our `/home/student` directory for this.

1.  **pwd** \- \[present working directory\] shows you what directory you are in.
    
    `student@bchd:~$` `pwd`
    
    `/home/student` 
    
2.  **ls** \- list out the contents of the current directory.
    
    `student@bchd:~$` `ls`
    
    `static` 
    
3.  **cd** \- \[change directory\] - allows you to move to a different directory. Here we can move to the static directory.
    
    `student@bchd:~$` `cd static`
    
4.  **mkdir** \- \[make directory\] - allows you to make a new directory. Let's make one called **training**.
    
    `student@bchd:~/static$` `mkdir training`
    
    Also, let's make sure we can see that we made this **training** directory.
    
    `student@bchd:~/static$` `ls`
    
    `training` 
    
    And let's move into the **training** directory.
    
    `student@bchd:~/static$` `cd training`
    
5.  **touch** \- makes a blank file.
    
    `student@bchd:~/static/training$` `touch example_01.txt`
    
    Verify that the file named **example_01.txt** is there now.
    
    `student@bchd:~/static/training$` `ls`
    
    `example_01.txt` 
    
6.  **echo** \- returns text to the standard output.
    
    `student@bchd:~/static/training$` `echo Alta3 Research Training rocks!`
    
    `Alta3 Research Training rocks!` 
    
    The `>` character allows us to redirect standard output to a different place, normally a file.
    
    `student@bchd:~/static/training$` `echo Alta3 Research has AWESOME labs! > myfile.txt`
    
    The `>>` characters allow us to redirect standard output and append it to the end of a file.
    
    `student@bchd:~/static/training$` `echo Alta3 Research has AMAZING labs! >> myfile.txt`
    
7.  **cat** \- \[concatenate\] prints file(s) to standard output.
    
    `student@bchd:~/static/training$` `cat myfile.txt`
    
    `Alta3 Research has AWESOME labs!
    Alta3 Research has AMAZING labs!` 
    
8.  **mv** \- \[move\] allows us to move a file or directory (often used to rename files).
    
    `student@bchd:~/static/training$` `mv myfile.txt ego_fuel.txt`
    
    Verify that the file has moved.
    
    `student@bchd:~/static/training$` `ls`
    
    `ego_fuel.txt example_01.txt` 
    
    Make sure that the contents of the file have not changed.
    
    `student@bchd:~/static/training$` `cat ego_fuel.txt`
    
    `Alta3 Research has AWESOME labs!
    Alta3 Research has AMAZING labs!` 
    
9.  **history** \- shows all of the commands performed in this shell session.
    
    `student@bchd:~/static/training$` `history`
    
     `1  # copy me
        2  pwd
        3  ls
        4  cd static
        5  mkdir training
        6  ls
        7  cd training
        8  touch example_01.txt
        9  ls
       10  echo Alta3 Research Training rocks!
       11  echo Alta3 Research has AWESOME labs! > myfile.txt
       12  echo Alta3 Research has AMAZING labs! >> myfile.txt
       13  cat myfile.txt
       14  mv myfile.txt ego_fuel.txt
       15  ls
       16  cat ego_fuel.txt
       17  history` 
    
10. **man** \- \[manual\] show the manual pages (aka documentation) for a given command. This is helpful for understanding any commands you may not feel comfortable with.
    
    `student@bchd:~/static/training$` `man ls`
    
    To quit out of this view, press the keyboard key **q**
    

Excellent work! Now, let's move back to the home directory before you start working on the next lab.

`student@bchd:~/static/training$` `cd ~`

Your prompt should now be back to: `student@bchd:~$`
