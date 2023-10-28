Git - Version control system

git         -   version control
github      -   hosting platform

So I am creating a project , where in the first day I have done the 5% , and in the next day 10% and 
within 10  days I completed the project . So after some months I decided to update the project but I only
need 50% from the start .So now what i want to do is to track all the files till the 50%  and want to remove 
everthing other than that.But that task will be hectic to do. In these type of scenarios if you use a version
control system like git then it will be easy for you . Just want to check commit number and revert the project
back to it. So studying git is important.

LIke restore point in windows.



1.Create a repository.
2.Open the folder in the pc where you want to clone the project.

    ==> two ways 

    1.open git bash there and -- git clone ----link-----

    2.in terminal ,first check if git is installed using git --version , then, git clone ----link----

      If not logged into the github then will ask the username and password , give that or set it 
      permnentyly in the windows credentials.
      Else give it as token.

        for that go to your github account --> settings --> Developer Settings --> Personal Access tokens
        ---> Token classic ---> generate new token ----> select the checkboxes ----> paste that in password

3.Check if repository is cloned

    git remote -v origin ( origin alias url )

4.Create , Update files for the project
5.After completing that day's work now we want to push that files to github
6.Before pushing you can check the status of files
    
    git status

    (there you can see a lot of untracked files ,Now we have to add these files into the staging)

7.for staging 

    ==> two ways

    1.add file_name 
      add file_name2   (add files indivudually)

    2.add .   (add all files at once with the dot)

8.Now check git status again and see all those files in the green color.Still the files are in the local 
  machine ,stll not added to github.

9.Now we have to commit the files , for committing add a message along with that to remember the current work
  done.

                         git commit -m 'message'

10.Now push

                         git push / git push origin master

11.Now go to the github repository and refresh the page and you can see all the files.


++  GIT LOG ++

                get the log     ==>      git log           (to exit from this 'q')

++ BRANCHING ++



When you create a repository by default your project will be either in branch 'main' or 'master'
so when creating a project each main steps create a new branch and work on it.so after completing it 
if you want that in project then only merge that with the project else won't include in the project.
or else if any error occur also it won't affect the project.



==> getting current branch                                                               -- git branch

==> create new branch                                                        -- git branch branch_name

==> switch branch                                                          -- git checkout branch_name

==> pushing the branch                                   -- git push --set-upstream origin branch_name

==> now to merge the branch with main/master                                  -- git merge branch_name

==> delete a branch                                                      -- git branch -d  branch_name

==> rename a branch                                                    -- git branch old_name new_name

==> Untrack a file                                                        -- git rm --cached file_name

==> commit and add in one line                                           --  git commit -a -m 'message' 

==> avoid a file while commiting add in the .gitignore file

==> revert back project to a commit                                 --   git reset --hard commit_number




++ force push ? ++

Sometimes the git our codes are not tracked  to overide that and push use --force




++ Now you want to update your project after sometime at that time give a ' git pull ' ++




