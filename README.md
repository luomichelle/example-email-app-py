
## Installation

Install Python 3.x.

Install source code:

```shell
git clone _________
cd example-email-app-py/
```

Install package dependencies:

```shell
pip3 install -r requirements.txt
```
## Setup

Follow the [Deployer's Guide](DEPLOY.md) to provision a new Heroku server, and configure the `SENDGRID_API_KEY` and `MY_EMAIL_ADDRESS` environment variables on the server and your local machine.

## Usage

Send me an email:

```shell
python3 app/email_me.py
```
