# jaiminho
A CLI tool for deployment notifications. Currently support Slack and New Relic

## Installing

```sh
$ curl https://raw.githubusercontent.com/emerleite/jaiminho/master/jaiminho > /path/to/jaiminho
```

## Slack Notification

First, you have to create a slack [incomming webhook](https://api.slack.com/incoming-webhooks).

jaiminho assumes you have a CHANGELOG.md based on https://keepachangelog.com/en/1.0.0/

After this initial setup, just ad to the end of your deployment script the following line:

```sh
$ DEPLOY_TAG="tag_number" DEPLOY_APP="Your APP" SLACK_HOOK_URL="https://hooks.slack.com/services/AAA/BBB/some_hash" ./jaiminho slack
```

## New Relic Notification

First, get your APP_ID API_KEY on New Relic settings.

Add the following line to the end of your deployment script:

```sh
$ DEPLOY_TAG="tag_number" NEW_RELIC_APP_ID="some_id" NEW_RELIC_API_KEY="some_api_key" ./jaiminho newrelic
```




