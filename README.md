# Example Email App - Python

## Prerequisites

Follow the [Setup Guide](SETUP.md) to obtain and configure credentials for using the SendGrid service to send email. And for configuring a machine to run this application.

## Installation

Install Python 3.x.

Install source code:

```shell
git clone git@github.com:s2t2/example-email-app-py.git
cd example-email-app-py/
```

Install package dependencies:

```shell
pip3 install -r requirements.txt
```

## Usage

Send yourself an email:

```shell
python3 app/email_me.py
```

## Deploying

Optionally follow the [Deployer's Guide](DEPLOYING.md) to run the application on a Heroku server previously created during the setup process.
