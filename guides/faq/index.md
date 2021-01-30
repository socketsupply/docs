# Frequently Asked Questions

## Who uses Operator Tools?

### Developers, Creatives, Managers, Founders

Cloud services like AWS are powerful, they provide a lot of utility,
but they're also very complex. They have a steep learning curve, and
are difficult to work with, even for experienced users.

Operator makes it easier to use the cloud to do things like deploy
your code, manage your static assets, and manage your data.

### Organizations

Operator isn't a service, it runs entirely within your network and
can be administered by your organization. Changes made with Operator
tools are sync'd between team members and can be reverted and exported
with <b>Operator Time Machine</b>.

## Why would anyone use a GUI? Do you even 1337??

Microsoft acquired a UI called Github for 7.5 Billion USD. People like GUIs.

## Do you collect telemetry data?

No! Use something like `Little Snitch` if you want to verify it. But our
reasons are that, like you, we have work to do and wouldn't want someone
watching over our shoulder as we do it. We collect no data what-so-ever
from you or about you, it's not our business.

## Do you audit the dependencies you use in your product?

Yes. Almost all of the deps we use, we also contribute to. If not, we
read the code. To make this more viable, we use as few dependencies as
possible. We also fork Elecron to remove dependencies that are
non-essential.

## How safe is your product?

Our products read only your data. We make sure your data is escaped
and properly contained when loaded. We don't load or execute any arbitrary
3rd party code. All our updates are signed and sent over encrypted channels.
Any opeartions that write data can be easily reverted using <b>Operator
Time Machine</b>.

## I like your UI, what framework did you use?

We are minimalists. We try to ship as little code as possible. We built our
own framework called [Tonic](https://tonic.technology).

## If I find a vulnerability, do you have a bug-bounty program?

Yes. Please email us at `infosec at optool dot co`.

## How can I improve the docs?

If you want to contribute to the docs, the repo is [here](https://github.com/optoolco/docs).

## How can I report an issue?

If you have found an issue, please report it on our [github beta](https://github.com/optoolco/beta/issues)
repository.

### Can I share the logs for the operator application ?

Yes, it would be very helpful if you took the local logfile for
the operator apps and [pasted it](https://gist.github.com/) to share
in the github issue.

You can find our log files on disk for

 - MacOS : `~/Library/Application Support/$APP_NAME/optoolco/logs.nldj`
 - Windows : `%appdata%\$APP_NAME\optoolco\logs.nldj`
 - Linux : `~/.config/$APP_NAME/optoolco/logs.nldj`

The `$APP_NAME` is one of ( `Operator`, `Buckets`, `Data` , `Functions` )

## How do I install Operator Tools?

### How do I download Operator Tools?

To download the software, visit the [downloads](/download) page.

### Does 5 Apps mean 5 copies of electron?

No. We only ship one binary. And we have a fork of electron that is much smaller and optimized for our use cases.

### How to install on macOS

- Download the <code>.dmg</code> file
- Navigate to your Downloads folder and double-click the <code>.dmg</code> to open
- When the installer appears, drag the Operator Icon onto the Applications folder to install
- Navigate to your Applications folder and double-click the Operator App Icon to open
- Eject the Operator installer

<notification-inline
  id="notification-macos-installation"
  dismiss="false"
  title="System Requirements"
  display="true">OS 10.9 or later
</notification-inline>

### How to installation on Windows

- Select Save or Save As to download the <code>.exe</code> file from the <a href="/downloads" alt="Downloads">downloads page</a>.
- If you select Save, the program file is in your Downloads folder.
- If you select Save as, you can choose where to save it.
- Launch from the Operator icon.

<notification-inline
  id="notification-macos-installation"
  dismiss="false"
  title="System Requirements"
  display="true">Windows 10 or later
</notification-inline>

### How to install on Linux

The following installers are available for Linux operating systems: <code>.AppImage</code>,
<code>.deb</code>, <code>.rpm</code>, and <code>.tar.gz</code>

How to install with .AppImage:

- Download the <code>.AppImage</code> file from the <a href="/downloads" alt="Downloads">downloads page</a>.
- Right click on the downloaded <code>.AppImage</code> file and select Properties.
- In the Permissions tab, check the box that says <b>Allow executing file as program</b>.
- Launch the application

<notification-inline
  id="notification-macos-installation"
  dismiss="false"
  title="System Requirements"
  display="true">64-bit Linux
</notification-inline>

### Can I install Operator on another computer?

With a single developer license, you can install operator on as many computers as you like.

### How to do a complete uninstall

You can use your OS to uninstall the application and then you can delete
the local files the applications have written

 - MacOS : `~/Library/Application Support/$APP_NAME/optoolco`
 - Windows : `%appdata%\$APP_NAME\optoolco`
 - Linux : `~/.config/$APP_NAME/optoolco`

You will have to delete them for `Buckets`, `Data`, `Functions` & `Operator`

### How to get the latest Operator updates.

The Operator Toolbox application checks for updates on a daily basis, if you
would like to update to the latest version immediately you can check for updates in the toolbox under the Preferences menu.

<img class="fullscreen" src="https://raw.githubusercontent.com/optoolco/docs/master/guides/faq/images/check-updates.png"/>

Once updates have been downloaded, you need to restart the app
to use the newest version of it.

## Accounts

### How do I change my password?

- Sign in to the <a href="/manage" alt="Management Page">management</a> page.
- On the <b>Account</b> tab, under <b>Password</b>, enter your old password and new password. Click <b>Save</b>.
- A code will be emailed to you. Enter it to confirm the change.

### I forgotten my password

- Proceed to the <a href="/management" alt="Management Page">management</a> page. If you are already signed in, click <b>Sign out</b>.
- On the Sign In page, click <b>Forgot Password</b> and follow the instructions.
- A code will be sent to your email for password reset.

## License

### What does my Operator license include?

A license includes access to all Operator applications, including periodic software updates.

## Applications

### How do I add multiple AWS accounts?

- Launch the Operator Toolbox application.
- Under the settings tab, select <b>AWS Profiles</b>.
- Type the name, key, and secret into the empty inputs and then click the check mark to save.

### How do I launch an app?

You can launch a Operator app from the toolbar application by selecting the <b>Launch</b> icon
next to the application.

### How do I install new Operator apps?

- Launch the Operator Toolbox application from your menu bar.
- At the left you will aee the apps, pick the one you want to download.
- Click the download button.
- After download, the app will launch.
- If you cannot select the download button, please check the status of your license.
