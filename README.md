## Quick Git Push from Terminal
A very simple and easy way to automate and make git push easy with just one line of command. 

### Bashrc configuration
Simple function that adds all the changes and pushes the changes. Add the scripts below at the end of your bashrc file. 
To access bashrc file:
`gedit ~/.bashrc`

```
gitpush()
{
echo "-----------------Adding all the changes-----------------------"
git add .
git commit -m "$*"
git push
}
alias easypush=gitpush
```
### Cache git username and password

```
git config credential.helper store
git push https://github.com/repo.git

Username for 'https://github.com': <USERNAME>
Password for 'https://USERNAME@github.com': <PASSWORD>

git config --global credential.helper 'cache --timeout 43200'
#it will be cached for 43200 seconds i.e.12 hrs

```
### Execution

Go to your git repo, open up a terminal and excute below to push changes.

For the first time run your bashrc changes, run
`source ~/.bashrc`

Then, excute git push commands with alias defined in the bashrc for easy execution

```
easypush "commit name"
```
And that's it. 

