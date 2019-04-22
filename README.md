# Bulldog
[Drupal VM](https://www.drupalvm.com/)

## Documentation

This version of Drupalvm is configured to run on Windows 10 and to install a drupal 8 site.

The site is accessed at: [http://drupal8vm.test/](http://drupalvm.8.abc.local/)

1. Clone the repository to your home folder on Windows 10
2. Open git bash command line (do not run as admin)
3. Navigate inside the folder
4. Run:
```
vagrant up
```
I ran into an error message after 'vagrant up' completed. Even so the box was up and i could access the site.

But the site was not fully configured. :-1:

So, I returned to git bash and ran:
```
vagrant up --provision
```
a couple of times.

Then everything worked. :smiley_cat:

### First tasks

1. Create a new PHPStorm project from existing files. Navigate to repo folder.
Use that as the root but the site docroot is the drupal/web folder inside the repo.

2. Run:
```
vagrant ssh
```
in git bash to login to the vagrant VM. You need to do this in order 
to run:
```
drush
drupal
```
The drupal command :muscle: runs the drupal console.
If you run a command and want to cancel it or indeed any command in git bash hold down:
```
Ctrl + C
```
If that does not work run:
```
Ctrl + D
```
Run: 
```
logout 
```
to get out of the vagrant VM back to your local file system.

### Module installation

There are two ways to install contributed modules:
- using the 'composer require' command
- Alternatively download the .zip file from the module's page on drupal.org. 
- copy it into modules/contrib/
- if there is no 'contrib' folder it is useful to create one and also a 'custom' folder 
- this organises your modules
