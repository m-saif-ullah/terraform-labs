 💻 SCM Option #1 - GitHub - Terraform 

### [Lab Objective](https://live.alta3.com/content/terraform/labs/content/github/simple-github-account-creation-zpatch.html#lab-objective)

In this lab, we're going to explore SCM, or Software Control Management platforms. Git is the de-facto tool for tracking and version controlling your work. Git is a tool that we run on our local machine. GitHub is an HTTPS browser-friendly platform that syncs with git, and makes your code available to the world. This is a good thing.

In this lab, you'll make a GitHub account. This is free and will allow you to save the code you develop this week.

### [Procedure](https://live.alta3.com/content/terraform/labs/content/github/simple-github-account-creation-zpatch.html#procedure)

1.  In your browser, open a new tab and navigate to [https://github.com](https://github.com/)
    
2.  If you already have an account with GitHub, sign in, and then skip to **Section 2 - Create a Repository**.
    

### [Section 1 - Create a GitHub account](https://live.alta3.com/content/terraform/labs/content/github/simple-github-account-creation-zpatch.html#section-1---create-a-github-account)

1.  Click on `Sign-up` on the landing page.
    
2.  Enter the following information.
    
    * **Email Address** \- Use an email address you check often.
    * **Password** \- Always make passwords unique and ultimately change them often.
    * **Username** \- This handle will be shared with career professionals.
3.  STOP: before you go any farther, record the above information. You will need it later.
    
4.  Now click on the **Create account** button at the bottom of the screen.
    
5.  At the bottom of the screen, click the green `Continue` button.
    
6.  Answer the questions as best you can to help the GitHub metrics, and then click `Submit` at the bottom of the screen.
    
7.  You'll need to verify your email address. Check the email address you used to sign up, and click on the link or button they sent to you.
    

### [Section 2 - Create a Repository](https://live.alta3.com/content/terraform/labs/content/github/simple-github-account-creation-zpatch.html#section-2---create-a-repository)

1.  Now that we have a verified GitHub account, let's try tracking some work. In the upper right hand corner, click on your profile icon, then on `Your Profile`. This is where you can choose to create a bio and a profile. This account is public and the world will look at your code, so be professional.
    
2.  In the center of the screen, click on the word `Repositories`, which is followed by a `0`.
    
3.  Click on the green `New` button, with the little book icon on it. This creates a repository. Repositories track work.
    
4.  Set the **Repository name** as `mycode`.
    
5.  Set the **Description** as something like, `Tracking my code`
    
6.  The repository should be set to **Public**.
    
7.  The README option is always best practice, so check the box. The objective is to describe what your repo contains.
    
8.  Change `Add a license: None` to `GNU General Public License v3.0`. Here's the TLDR, "We're comfortable with the world borrowing our code, provided they give us credit, should it get used."
    
9.  Now click the green `Create repository` button at the bottom of the screen.
    
10. You should see your repository `mycode`.
    
11. GitHub lets you have friends just like other social media platforms. Checkout & follow all (or at least your) Alta3 instructors:
    
    * [Zach](https://github.com/rzfeeser)
    * [Chad](https://github.com/csfeeser)
    * [Tim](https://github.com/BicycleWalrus)
    * [Jason](https://github.com/JasonTrespel)
12. You might try asking some fellow students for their usernames and repeating the above steps.
    

### [Section 3 - Create a Personal Access Token](https://live.alta3.com/content/terraform/labs/content/github/simple-github-account-creation-zpatch.html#section-3---create-a-personal-access-token)

1.  Create your Personal Access Token.
    
2.  Click on your avatar, it looks like a `tiny round icon in the upper right corner`
    
3.  Click `Settings` on the dropdown
    
4.  Click `Developer settings` on the bottom of the left menu
    
5.  Click `Personal access tokens`
    
6.  Click `Tokens (classic)`
    
7.  Click `Generate new token`
    
8.  Click `Generate new token (classic)`
    
9.  Title the key to "tmux access to github"
    
10. Check the box for `repo`
    
11. Click the green `Generate token` button at the bottom
    
12. The token will be displayed at the top of the page. **Leave this page open for now** it will only display the token once, and we'll need it in a moment...
    

### [Section 4 - Sync your Terminal to GitHub](https://live.alta3.com/content/terraform/labs/content/github/simple-github-account-creation-zpatch.html#section-4---sync-your-terminal-to-github)

1.  Return to your Alta3 Terminal now.
    
2.  Set the tool git so that it always remembers the password (or token) we use.
    
    `student@bchd:~$` `git config --global credential.helper store`
    
3.  Replace the `Mona Lisa` with your GitHub username and THEN run this command. This provides _metadata_ to your commits, and it is not critical that it be your GitHub username, but should identify you.
    
    `student@bchd:~$` `git config --global user.name "Mona Lisa"`
    
4.  Replace the `monalisa@example.com` with your email address and THEN run this command. This provides _metadata_ to your commits, and it is not critical that it be the email you signed up with, but should help identify you.
    
    `student@bchd:~$` `git config --global user.email "MonaLisa@example.com"`
    
    > You are all set up for git cloning and pushing your personal repos.
    
5.  You have to clone into an empty directory. This step just ensures the `~/mycode` name isn't taken.
    
    `student@bchd:~$` `mv ~/mycode/ ~/mycode-backup/ 2>/dev/null`
    
    > The 'mv' is move, ~/mycode/ is the source, ~/mycode-backup/ is the new name, and 2>/dev/null supresses any error, which might occur if you do not already have a ~/mycode folder.
    
6.  Customize the following link. It's as simple as replacing `YOUR USER NAME` in `https://github.com/YOUR USER NAME/mycode` with your username from GitHub, _or_, just copying the URL at the top of your browser, when you're looking at your mycode repository on GitHub.
    
    `student@bchd:~$` `git clone https://github.com/YOUR USER NAME/mycode ~/mycode`
    
    > If you run into an error with this step, read the instructions once more and try it again!
    
7.  When prompted for a username and password, the username is your **GitHub username** and the password is the **TOKEN** you created earlier. Paste your token when prompted, and remember that in Linux passwords are not displayed when typed!
    
8.  You should now have a new folder (mycode) in your home directory. Move into it.
    
    `student@bchd:~$` `cd /home/student/mycode/`
    
9.  Great! Try making a file we can commit
    
    `student@bchd:~$` `touch /home/student/mycode/alta3research.txt`
    
10. The following steps are ones you should memorize. You'll be issuing these commands all the time. First issue `git status`, which will reveal if you added something and forgot about it.
    
    `student@bchd:~/mycode$` `git status`
    
11. Next we'll describe what we want to add to our repo. We'll wildcard this, so everything in the `~/mycode/` directory is added.
    
    `student@bchd:~/mycode$` `git add *`
    
12. Time to perform a commit. This makes a new version.
    
    `student@bchd:~/mycode$` `git commit -m "First commit to learn about version controlling"`
    
13. Now push your new version to GitHub for tracking. By default, the keyword **origin** points to the repo you cloned the repo from.
    
    `student@bchd:~/mycode$` `git push origin HEAD`
    
14. Type in your GitHub username.
    
15. Paste in the GitHub token you generated earlier. _You will not have to type this in again, it will be cached_
    
16. Go up to GitHub, and you should see the file `alta3research.txt` has appeared in your repository.
    
17. Great! Move back to your home directory.
    
    `student@bchd:~/mycode$` `cd`
    
