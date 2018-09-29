# Voyager Installer

This simple little script is a fork of github.com/laravel/installer.
Version numbers will be bumpped based on Laravel's installer numbers since I plan to keep them in sync.

## About & Why
I have recently doing a number of small quick projects using Voyager and Laravel. They are all, at most a week's worth of work and I find it boring to install Laravel, then Voyager and iSeed every time I need to spin up a new project.

This porject is, very basically, the Laravel Installer with added requirements to composer.json
This way, you can quickly get up to speed with a voyager project the same way you would with a Laravel one.

## What is here?

Basically we have the Laravel installer default instalation with an added tcg/voyager package and orangehill/iseed.

Voyager, as the name of the installer suggests is the basic require for Voyager Admin.

iSeed is a simple but nevertheless essential install for anybody doing serious Laravel/Voyager work.

## How to use it?

Do like you would with Laravel...

```
voyager new project-name
```

This will create a new project folder **project-name** in the current directory, all ready with the dependencies installed.. Follow the short instructions at the end of the installer and get up and running in a jiffy.

## Quick install overview

### Step 1 - Create a new project
```
voyager new project-name
```
### Step 2 - Database and .Env
Create a database for use with your project and edit your .env file in the root of your project folder.

### Step 3 - Install Voyager
from the root of your project directory
```
php artisan voyager:install
```
to install a default blank voyager project or
```
php artisan voyager:install --with-dummy
```
to install some sample data in your voyager instalation.

### Step 4 - Create and Admin User
If you are using a blank install (like you most usually will), run this interactive command to create a user for your administration area. (repalce email@email.com with your desired email)
```
php artisan voyager:admin email@email.com --create
```
Just  answer the questions the interactive shell asks you and you're all setup.

If you installed dummy data, the user is **admin@admin.com** and the password is **password**

Your login url is "http://yoursite/admin"

## To Do and considerations
It would be nice to add a few extra things to this command line. Have it add information to the welcome screen for the laravel instalation would be nice (replace the default with my own version explaining the next steps and so on)

Have the option of creating a database automatically when you initiate a new project would also be nice maybe. Probably with an interactive prompt or something.

Please feel free to use this at your will.
