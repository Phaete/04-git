How have you versioned your files so far (without Git)?

    Yes, only with Git/Github.

What are best practices for the ideal commit message?

    Be precise, keep it short, write in imperative

You want to save a version that adds the feature to your pet management app that now allows
managing multiple pets per person. How would you name the commit?

    Commit message would be something like: Add function to manage multiple pets per person

Estimate: how many commits will you create during the bootcamp? Please provide a rough estimate with your calculation.

    ~150-200

You accidentally did not include the .idea folder in the .gitignore file and committed
these files as well. Now they are stored in the Git commit.
How can you remove these files from the commit?
(This requires a few commands on the command line, please research them on the internet or with ChatGPT and enter them here - it's okay if they don't work, we will try them together)

    // 1-3 will also delete the commit
    1. 'git log' to view the commit history and find the relevant hash
    2. 'git reset --soft HEAD~1' to go back 1 commit
    3. 'git reset HEAD .idea' to unstage the .idea folder
    4. 'git rm -r --cached .idea' to completely remove the .idea folder from the staging area
    5. 'git commit -m "Exclude .idea folder from commit"' to commit the changes without the .idea folder


Create a shared Git repository on GitHub and work on it as a team. Come up with a creative name for the repo. Each team member should make changes to the code and create commits.
Invite your team members to the repository. Please enter the link to the repository here:

    https://github.com/Phaete/04-git-teamchallenge

One of you should now clone the repository to their local machine. Add a new text file with some lines of text.
Create a commit to save your changes and leave a meaningful commit message.
Push the commit to the shared repository on GitHub.

Another team member should now clone the repository to their local machine. Modify the file that your team member added. Create a commit to save your changes and leave a meaningful commit message. Push the commit to the shared repository on GitHub.

Each team member should now fetch the latest changes from the repository and see the file.

    [Done]

Now make changes simultaneously. Create a commit each. Push these commits.

At what point are conflicts displayed?


    At the time of editing the file?

    At the time of creating the commit?

    At the time of pushing? <--

    At the time of pulling? 


Did you expect this point in time? Can you explain it briefly, or do you have any questions about it?

    If we push a commit, the commit assumes that the previous commit had the "head" tag, but it's not there anymore, it's on another commit, made by someone else, so the only option is to resolve the conflict.

Use IntelliJ to resolve the conflicts (which can be easier or harder depending on the changes). Take a close look at the conflict resolution dialogs and try to understand them.

    Merge vs Rebase


# Bonus:
Now create a new Java application in IntelliJ. You can share the project on GitHub through IntelliJ's "VCS" menu.

Write an application that outputs a calendar.

Each row represents a week, each column represents a weekday. The year starts with Monday. The year is not a leap year. Output the months from January to December. The output should look like this:

```
Januar
Mo Di Mi Do Fr Sa So
1  2  3  4  5  6  7
8  9 10 11 12 13 14
15 16 17 18 19 20 21
22 23 24 25 26 27 28
29 30 31

Februar
Mo Di Mi Do Fr Sa So
         1  2  3  4
5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28

... und so weiter
```

Proceed as follows:


    Team member A creates the project and uploads it to GitHub.

    Team member B clones the project and creates a new class. The main method should output the strings "January" to "December".

    Team member C clones the project and creates a method printCalendarForMonth(String monthName), which outputs the name of the month for each month, and is called 12 times in the main method with different parameters.

    Team member D clones the project and adds to the method so that it also outputs the row with the weekday names (Mo Tu We Th Fr Sa Su).

    Team member A pulls the project and adds to the method so that it outputs a row with numbers 1-7 below the weekday names.

    Team member B pulls the project and extends the method so that it continues counting the numbers in the following rows, up to the value of the parameter int daysInMonth (values 28-31).

    Team member C pulls the project and extends the method so that the counting does not always start with Monday, but can be shifted with the parameter int offsetDays (values 0-6).

    Team member D pulls the project and enjoys the output.


Please note:


    If you are not a team of four, just rotate more often (team member A takes on tasks 1, 4, 7).

    The task is intended to help you understand Git and GitHub. Do not try to solve the task on your own, but work on it together. Collaboration is the learning objective here.


Now add all imaginable features that come to your mind. Here are a few ideas:


    Input of a year via Scanner and System.in

    Determining whether the year is a leap year

    Calculation of the weekday for January 1st of the year

    Highlighting holidays, including movable holidays

    Support for multiple languages

    Variable column width (width 2 for Mo, width 3 for Mon, width 6 for Monday)

