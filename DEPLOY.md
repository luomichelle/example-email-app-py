# Deployer's Guide

Adapted from https://devcenter.heroku.com/articles/sendgrid#provisioning-the-add-on.

## Prerequisites

### Provision Heroku Server

Install Heroku CLI.

Login to Heroku from the CLI:

```shell
heroku login # then enter your Heroku username and password (and optionally enter your MFA code)
```

Provision a new Heroku server:

```shell
heroku apps:create example-email-app-py # use your own unique name instead of `example-email-app-py`, or omit the name and heroku will choose a fun one for you
```

Provision the Heroku server to use the "SendGrid" email service:

```shell
heroku addons:create sendgrid:starter -a example-email-app-py # specify app name only if you control multiple applications
```

### Obtain SendGrid API Key

Get SendGrid credentials:

```shell
heroku config:get SENDGRID_USERNAME
heroku config:get SENDGRID_PASSWORD
```

Visit the [SendGrid Apps Management Console](https://app.sendgrid.com/settings/api_keys) and use the credentials to sign in!

Click the "Create API Key" at the top right of the page. Note the resulting "API Key", and copy it to your computer's clipboard.

### Configure Environment Variables

Configure both your local machine and the Heroku server to use the API Key by specifying an environment variable on each called `SENDGRID_API_KEY`. Use an operating-system-specific process to configure your own machine. As for configuring the Heroku server:

```shell
heroku config:set SENDGRID_API_KEY="xxxx_api_key_xxxx" -a example-email-app-py # specify app name only if you control multiple applications
```

Because the application needs an email address to send mail to and from, also specify your email address in an environment variable on each called `MY_EMAIL_ADDRESS`. Use an operating-system-specific process to configure your own machine. As for configuring the Heroku server:

```shell
heroku config:set MY_EMAIL_ADDRESS="your_address@gmail.com" -a example-email-app-py # specify app name only if you control multiple applications
```

At this time, you should be able to run the app from your local machine and it should use the SendGrid service to send you an email! Note: it may take a few minutes.

## Deploying

TBA
