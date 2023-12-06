[Using Vi and Vim](https://live.alta3.com/content/terraform/labs/content/vim/vim-basics.html#using-vi-and-vim)
==============================================================================================================

Throughout the course, you'll find our documentation suggests using the vim text editor. Vim is an improved version of vi, so if you know vi, you'll just be refreshing some basic skills in this lab.

Vim is the editor of choice for many developers and power users. It's a "modal" text editor based on the vi editor written by Bill Joy in the 1970s for a version of UNIX. It inherits the key bindings of vi, but also adds a great deal of functionality that is missing from the original vi.

In most text editors, the alphanumeric keys are only used to input those characters unless they're modified by a control key. In vim, the mode that the editor is in determines whether the alphanumeric keys will input those characters or move the cursor through the document. This is what is meant by 'modal.' When you first enter vim, you enter in the command mode.

[Procedure - Using Vim](https://live.alta3.com/content/terraform/labs/content/vim/vim-basics.html#procedure---using-vim)
------------------------------------------------------------------------------------------------------------------------

1.  Review _**(read-only)**_ the following **vim** commands:
    
    * **To start editing changes by entering the --INSERT-- mode:**
        
        * press `i`
    * **To stop editing and return to command mode:**
        
        * press `ESC`
    * **To save and quit:**
        
        * press `SHIFT` \+ `:` _press SHIFT and the COLON keys at the same time_
        * type `wq` (write out and quit)
        * press `ENTER` to confirm
    * **To quit without saving:**
        
        * press `SHIFT` \+ `:` _press SHIFT and the COLON keys at the same time_
        * type `q!` (quit and ignore all changes)
        * press `ENTER` to confirm
2.  Move to the student home directory.
    
    `student@bchd:~$` `cd`
    
3.  Now create a text file within the vim environment.
    
    `student@bchd:~$` `vim zork.test`
    
4.  Vim is entered in command mode. To write text, you'll need to change to **--INSERT--** mode. To begin writing text, press:
    
    * `i`
5.  Notice in the bottom left corner of the screen it now says **--INSERT--**
    
6.  Type a few sentences. Be sure to include some carriage returns, like the following:
    
    `West of House
    You are standing in an open field west of a white house, with a boarded front door.
    There is a small mailbox here.` 
    
7.  Okay, great! Now leave **--INSERT--** mode, and return to command mode, by pressing the escape key.
    
    * `Esc`
8.  Notice that **--INSERT--** no longer is at the bottom left of the screen. Generally, pressing the Escape key will always return you to the command mode.
    
9.  Use the directional arrow keys on the keyboard to move the cursor around the screen.
    
10. Perform the following to save changes, and return to the command line.
    
    * press `SHIFT` \+ `:`
    
    > _press SHIFT and then the COLON key at the same time_
    
    * type `wq` (write out and quit)
    * press `ENTER` to confirm
11. Confirm the file saved correctly by printing its contents. We can use the **cat** command to catenate, or read data from files and print their contents to the screen.
    
    `student@bchd:~$` `cat zork.test`
    
12. Edit the file zork.test again.
    
    `student@bchd:~$` `vim zork.test`
    
13. Remember, you enter vim in command mode. Take advantage of that and press the following capital letter to jump to the end of the file:
    
    * press `SHIFT` \+ `g`
    
    > _press SHIFT and the g keys at the same time_
    
14. Press the following capital letter to begin appending at the end of the line (enter --INSERT-- mode at the end).
    
    * press `SHIFT` \+ `a`
    
    > _press SHIFT and the a keys at the same time_
    
15. You'll notice it says **--INSERT--** at the bottom left of your screen again. Once again you can type normally. Add additional text, such as the following:
    
    `West of House
    You are standing in an open field west of a white house, with a boarded front door.
    There is a small mailbox here.
    Open mailbox
    Opening the small mailbox reveals a leaflet.
    Read leaflet
    (leaflet taken)
    "WELCOME TO ALTA3 LABS!"` 
    
16. Okay, great! Now leave **--INSERT--** mode, and return to command mode by pressing the escape key.
    
    * `Esc`
17. Perform the following to return to the command line **without** saving any changes.
    
    * press `SHIFT` \+ `:`
    
    > _press SHIFT and the COLON keys at the same time_
    
    * type `q!` (quit without saving)
    * press `ENTER` to confirm
18. Confirm that none of the changes you just made were saved.
    
    `student@bchd:~$` `cat zork.test`
    
19. Remove the file.
    
    `student@bchd:~$` `rm zork.test`
    
20. Review a vim cheat sheet. These make very useful wall art and you may have seen one hanging in a colleague's workspace.
    
    [![](./2  Vim_ A Modal Text Editor - Terraform_files/vim.png)](https://alta3.com/s/vim-t4xp.pdf)
    
    > Get all of Alta3's Cheat Sheets here! [https://alta3.com/posters](https://alta3.com/posters)
    
21. Don't worry if you got stuck a few times, go back and try it again! Working within the vim environment is a basic Linux admin skill that is useful to everyone that expects to work at the Linux CLI.
