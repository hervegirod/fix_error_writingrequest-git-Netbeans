# Overview
Explain how to fix the git dreaded "Error writing request body to server" in Netbeans when  trying to push

# Use case
You encounter an "Error writing request body to server" when trying to push a git repository on Netbeans

# How to fix it on Netbeans
You have to increase the http post buffer size in the "Open Configuration" (on .git/config) by adding these lines:

    [http]
        postBuffer = 524288000

# How to fix it on git prompt
Add the associated global configuration:

    git config --global http.postBuffer 524288000

# Example
See the file

# Reference
see https://bz.apache.org/netbeans/show_bug.cgi?id=216957

see https://stackoverflow.com/questions/6842687/the-remote-end-hung-up-unexpectedly-while-git-cloning

