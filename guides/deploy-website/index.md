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
