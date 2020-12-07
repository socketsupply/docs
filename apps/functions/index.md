# Functions

The _Functions_ app helps you deploy and manage serverless code.


## Create a Function

To create a function, choose `Create` from the `Actions` menu.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/create.png"/>


## Git Integration

Enabling git integration will ensure you and your team are
always working with the latest version of the code.


### New Functions

If you create a new function that points to a directory on your
computer and that code is initalized as a git repository, the
Functions app can automatically detect your remote. All you have
to do is click the toggle labeled `Git Integration`.

If you create a new function and don't have any code on your
computer, you can get it by entering the remote and clicking the
`Git Integration` toggle.


### Existing Functions

If you create a new function that points to a directory on your
If someone else created the function using the Functions app,
you will see the remote already entered into the input and you
can click the `Git Integration` toggle.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/view-setup.png"/>


## Quick Edit

The Functions app will show you the files form your function in
the tree. The app isn't inteneded to replace your editor but in
some cases it's convenient to quickly view or edit source files.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/editor.png"/>


## Configuration


### API

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/view-api.png"/>

### Permissions

TODO


## Deploying

When you are ready to deploy, go to the main menu and select `Code`
and then `Deploy`. 


### Preparing for Production

The total number of concurrent connections for all functions in
a particular region is, by default, limited to 100. This limit is
a guard-rail that AWS puts in place by default to protect you from
run-away costs. If you want to increase the limit, follow the steps
found in [this][0] guide.


## Log output

You can log to `stdout` or `stderr` from any function. Logs are
piped to CloudWatch and you can tail them immediately using the
built-in console. The console shoud correctly highlight JSON and
other notable things that you log.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/apps/functions/images/view-logs.png"/>

[0]:http://docs.aws.amazon.com/lambda/latest/dg/concurrent-executions.html#increase-concurrent-executions-limit
