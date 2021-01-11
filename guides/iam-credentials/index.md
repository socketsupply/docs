# Setting up AWS credentials for operator.

One of the upcoming features is an IAM wizard that will help
walk you through setting up the AWS IAM permissions to get the
most of the Operator applications.

In the meanwhile, here's a short guide in how to setup a user
and a role to use the operator applications.

## Creating an operator policy

To avoid giving the Operator tools access to your entire AWS account you can create a policy that includes only the permissions
that the operator tools need.

Start by going to IAM and clicking on policies and then create policy

<img src="https://raw.githubusercontent.com/optoolco/docs/master/guides/iam-credentials/images/iam-create-policy.png"/>

Then you want to copy our recommended policy JSON into the JSON
editor in the AWS console

You can [find our policy here for now](https://gist.github.com/Raynos/d34165abdb8336c451e239215f802e64)

<img src="https://raw.githubusercontent.com/optoolco/docs/master/guides/iam-credentials/images/iam-policy-json.png"/>

Give the policy a name, I would recommend `OperatorToolsAccess`
and then review/save it.

## Creating a CLI user for the Operator apps.

With a IAM policy created you can create a new user with it's
AWS access key and AWS secret.

Go to the IAM users section and click create user.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/guides/iam-credentials/images/iam-create-user.png"/>

Then enter a name for your user and enable programattic access.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/guides/iam-credentials/images/iam-new-user.png"/>

When setting permissions, go to the attach a policy tab and find
the `OperatorToolsAccess` role that you have created and select it.

<img src="https://raw.githubusercontent.com/optoolco/docs/master/guides/iam-credentials/images/iam-user-permissions.png"/>

You can skip tags and then review the IAM user to be created.

Once the user is created you will see the access key & secret
credentials

<img src="https://raw.githubusercontent.com/optoolco/docs/master/guides/iam-credentials/images/iam-user-created.png"/>

## Using credentials in Operator app.

You can import these credentials into the Operator toolbox under
`Settings` => `AWS Profiles`

There's a section in the [getting started guide](https://optool.co/docs/?get-started/running-operator-toolbox) about adding credentials.
