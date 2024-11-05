## git_basics
*General things to know about Git and GitHub*

When working with two Local and Remote repositories on one Project, it is crucial to understand, how Git and GitHub work.

For example :
Working on a single Project:

# In Computer 1(not a personal computer or System):
Remote repo created in Computer 1  : *remote1* 
                          with URL : *remote_url1*
Consider remote1 as the submission repository.

The second remote repo, which is your personal GitHub repository  : *remote2*
                                                        with URL  : *remote_url2*

Now you clone the remote1 using remote_url1 : *local1*
        git clone [remote_url1] [local1]

Add the other remote repository - remote2
        git remote add [a_repo_name] [remote_url2]
In the command, we can modify it as:
        git remote add remote2 remote_url2

When you execute the above command. List the remotes on Computer 1 to confirm their names and URLs. Run this on Computer 1:
      git remote -v

You will get something like this:                         In the above case:
    [a_repo_name] remote_url2 (fetch)                                     remote2 remote_url2 (fetch)
    [a_repo_name] remote_url2 (push)                                      remote2 remote_url2 (push)
    origin remote_url1 (fetch)                                            origin remote_url1 (fetch)
    origin remote_url1 (push)                                             origin remote_url1 (push)

Now you can push separately to both Remote repos from one local repository in Computer 1:
        git push    // pushes to origin
        git push remote2  // pushes to the remote 2 with the commit changes and messages


So if you want to update both remote repos at one git push command, then configure it like the below:
      git remote set-url --add --push remote2 remote_url2
then you need to use the git command : *git push* which pushes to both remote repos at once without mentioning the remote repo name.

Similarly in computer 2, we have to do the same.

# In Computer 2 (Personal Computer):
remote repo - Personal GitHub repository: *remote1*
                                with URL:  *remote_url1*
      remote repo -submission repository: *remote2*
                                with URL:  *remote_url2*

Now you clone the remote1 using remote_url1 : *local1*
        git clone [remote_url1] [local1]

Add the other remote repository - remote2
        git remote add [a_repo_name] [remote_url2]
In the command, we can modify it as:
        git remote add remote2 remote_url2




