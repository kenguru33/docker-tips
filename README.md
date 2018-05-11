### Docker Tips

#### Run composer and bower etc.. as local installed through a docker container
Create alias to run container wihout typing docker run ...

##### Example with composer:

Windows (Powershell):
```
function composer {docker run -it --rm --volume ${PWD}:/app composer }
```
Mac OS:
```
alias composer docker run -it --rm --volume $PWD:/app composer install
```
Linux:
```
alias composer='docker run -it --rm --volume $PWD:/app --user $(id -u):$(id -g) composer'
```

To make alias/functions persistent just put them in .bash_aliases if using bash. For windows, edit $profile. (eg: notepad $profile)

Now you can type composer as it is installed locally!