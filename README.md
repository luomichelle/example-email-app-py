
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

## Setup

Follow the [Deployer's Guide](DEPLOY.md) to provision a new Heroku server, configure the SendGrid email service, and configure the `SENDGRID_API_KEY` and `MY_EMAIL_ADDRESS` environment variables on both the server and your local machine.

## Usage

Send me an email:

```shell
python3 app/email_me.py
```
