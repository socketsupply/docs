# Functions

The _Functions_ app helps you deploy and manage serverless code.

## Create a Function

To create a function, choose `Create` from the `Actions` menu.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/create.png"/>

> Note: If you don't have any code locally, you can enter the
> `git remote` and it can be sync'd automatically for you.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/view-general.png"/>

## Log output

You can log to `stdout` or `stderr` from any function. Logs are
piped to cloud watch and you can view them immediately using the
built-in console.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/console.png"/>

The console shoud correctly highlight JSON and other notable things.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/console-highlights.png"/>

## Quick View/Edit

The Functions app will show you the files form your function in
the tree. The app isn't inteneded to replace your editor but in
some cases it's convenient to quickly view or edit source files.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/editor.png"/>
