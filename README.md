# Serverless Telegram Bot

A basic serverless [Telegram bot](https://core.telegram.org/bots) using [Google Cloud Functions](https://cloud.google.com/functions/).

This bot runs with Python 3.9 and [python-telegram-bot](https://python-telegram-bot.org/).

See https://seminar.io/2018/09/03/building-serverless-telegram-bot/ for more details about this bot.

## Deploy

```
$ sudo gcloud  functions deploy webhook --set-env-vars "TELEGRAM_TOKEN=xxxxx:xxxxx" --runtime python39 --trigger-http --project PROJECT_NAME
```

and then type (change accoridingly)
```
$ curl "https://api.telegram.org/botxxx:xxxx/setWebhook?url=https://us-central1-telegram-xxxx.cloudfunctions.net/webhook"
```

## Testing

```
$ pip install -r requirements-test.txt
$ python test_main.py
```
