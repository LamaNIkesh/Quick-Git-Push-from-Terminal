## Quick Git Push from Terminal

### Bashrc configuration
Simple function that add all the change and pushes the changes

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
