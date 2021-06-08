# Deploying a website with Operator

From the `Files` application you can deploy your website project.

The first step is to navigate to the bucket you want to host your
website files in and select `Website Hosting` in the properties panel. Then click the link to start deploying your website.

<img class="fullscreen" src="https://raw.githubusercontent.com/optoolco/docs/master/guides/deploy-website/images/bucket-properties.png"/>

## Deploying files directly.

Operator uploads your website files, if you have the HTML/CSS/JS
files available, you can upload them directly and skip the build step

<img class="fullscreen" src="https://raw.githubusercontent.com/optoolco/docs/master/guides/deploy-website/images/no-build-step.png"/>

Without the build step, you can select the file location and then
continue to deploy your files.

## Deploying files with a build step.

If your project uses framework or has a build step that outputs
static assets that can be uploaded, you will want to tell operator
what command to run for your framework.

<img class="fullscreen" src="https://raw.githubusercontent.com/optoolco/docs/master/guides/deploy-website/images/build-step.png"/>

Instead of telling Operator where the files are to upload, Operator
will tell you where to write the output of the build step to.

This is done with the `OPTOOLCO_BUILD_OUTPUT` environment variable. Your
build step needs to write files to that directory. As an example, if your
using `next` your build step would look like

```sh
next export -o $OPTOOLCO_BUILD_OUTPUT
```
