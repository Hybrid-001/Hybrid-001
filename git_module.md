    We'll walk through developing a simple project that has been split up into a main project and a few 
sub-projects.

    Let's start by adding an existing Git repository as a submodule of the repository that we're working on.
To add a new submodule you use the git `submodule add command` with the absolute or relative URL of the 
project you would like to start tracking. In this example, we'll add a library called "hybrid_submodule".

    ```
    $ git submodule add git@github.com:Hybrid-001/hybrid_submodule.git

    ```
    By default, submodules will add the subproject into a directory named the same as the repository, in this 
case "hybrid_submodule". You can add a different path at the end of the command if you want it to go elsewhere.


    If you run git status at this point, you'll notice a few things.

    ```
    $ git status

        On branch master
        You branch is up-to-date with 'origin/master'

        Changes to be committed:
            (Use "git reset HEAD <file>..." to unstage)

            new file: .gitmodules
            new file: hybrid_submodule

    ```

    First, you should notice the new .gitmodules file. This is a configuration file that stores the mapping 
    between the project's URL and the local subdirectory you've pulled it into:
 
     [submodule "hybrid_submodule"]
            path = hybrid_submodule
            url = git@github.com:Hybrid-001/hybrid_submodule.git

    If you have multiple submodules, you'll have multiple entries in this file. It's important to note that 
this file is version-controlled with your other files, like your .gitignore file. It's pushed and pulled with 
the rest of your project. This is how other people who clone this project know where to get this submodule
projects from.


    This other listing in the git status output is the project folder entry. If you run git diff on that, you 
see something interesting.

    ``` 
    $ git diff --cached hybrid_submodule

    ```

    Although hybrid_submodule is a subdirectory in your working directory, Git sees it as a submodule and 
doesn't track its contents when you're not in that directory. Instead, Git sees it as a particular commit from
that repository.

    If you want a little nicer diff output, you can pass the --submodule option to git diff

    ``` 
    git diff --cached --submodule

    ```
    When you commit, you see something like this:

    ```
        $ git commit -am "Add submodule "

        [.....] Add hybrid_submodule module
        2 files changed, 4 insertions(+)
        create mode 1000644 .gitmodules
        create mode 1600000 hybrid_submodule

    ```

    Notice the 1600000 mode for the hybrid_submodule entry. That is a special mode in Git that basically 
means you're recording a commit as a directory entry rather than a subdirectory or a file.

    Lastly, push these changes:
    ```
        $ git push origin master
    ```
    
    Cloning a Project with Submodules

    ```
    $ git clone git@github.com:Hybrid-001/hybrid_submodule.git

    $ cd hybrid_submodule

    $ git submodule init

    ```
    Now your hybrid_submodule subdirectory is at the exact state it was in when you commited earlier

    There is another way to do this which is a litter simpler, however, If you pass --recursive -submodule 
to the git clone command, it will automatically initialize and update each submodule in the repository, including
nested submodules if any of the submodules in the repository have submodules themselves.

```
   $ git clone --recursive -submodules git@github.com:Hybrid-001/Hybrid-001.git

```
    If you aleady cloned the project and forgot --recursive-submodules, you can combine the git submodule init
and git submodule update steps by running git submodule update --init. To also initialize, fetch and checkout 
any nested submodules, you can use the foolproof 

``` 
$ git submodule update --init --recursive 

```
    If you run git submodule update --remote, Git will go into your submodules and fetch and update for you 
    ``` 
    $ git submodule update --remote hybrid_submodule


    ```


    If you want to see more, visit : https://git-scm.com/book/en/v2/Git-Tools-Submodules#:~:text=If%20you%20want%20to%20check,to%20update%20the%20local%20code.&text=Now%20if%20you%20go%20back,that%20were%20added%20to%20it.
    
    Use to git pull the submodule changes 

    ```
        $ git submodule foreach git pull origin main:main

    ```





























