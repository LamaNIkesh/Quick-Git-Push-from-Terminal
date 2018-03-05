## Quick Git Push from Terminal

### Bashrc configuration
Simple function that add all the change and pushes the changes. Add the scripts below at the end of your bashrc file. 
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
