# [5 Ways to DevOps-ify your App - Github Actions Tutorial; Fireship](https://www.youtube.com/watch?v=eB0nUzAI7M8)

## What is Github Actions?

Github Actions, are like Plugins or Extensions which are triggered on an event which takes place on a github repo, that automates a process or workflow.

Github Actions, can be fould under the Actions tab on the top navigation of any Github repo.

### 1. Continuous Integration

CI - Merge Code In

Inside the repo: `.github/workflows/integrate.yml`

````
name: Node Continues Integration

on:
    pull_request:
        branches: [ master ]

jobs:
    test_pull_request:
        runs-on: ubuntu-latest
        steps:
            - uses: actions/checkout@v2
            - uses: actions/setup-node@v1
                with:
                    node-version: 12
            - run: npm ci
            - run: npm test
            - npm: run build
````

`git add .`
`git commit -m "feat: ci workflow"`
`git push origin master`

Write/Break Code...

`git checkout -b testing`
`git add .`
`git commit -m "this should break it"`
`git push origin testing`

Compare & pull request

It will mention, 'Some checks haven't completed yet'

If you click "details" it will show you what it is doing.

Write/Fix Code...

`git checkout -b testing`
`git add .`
`git commit -m "fixed it!"`
`git push origin testing`

This will re-run the code and hopefully fix it.

### 2. Continuous Deployment

CD - Release Code Out

`firebase init`

`firebase deploy --only hosting`

`firebase login:ci` to get a token

Settings

Secrets

Add a new secret

Name: FIREBASE_TOKEN
Value: your-token

Inside the repo: `.github/workflows/deploy.yml`

````
name: Firebase Continuous Deployment

on:
    push:
        branches: [ master ]

jobs:
    deploy:
        runs-on: ubuntu-latest
        steps:
            - uses: actions/checkout@master
            - uses: actions/setup-node@master
                with:
                    node-version: 12
            - run: npm ci
            - run: npm run build
            - uses: w9jds/firebase-action@master
            with:
                args: deply --only hosting
            evn: 
                FIREBASE_TOKEN: ${{ secret.FIREBASE_TOKEN }}
````

`git add .`
`git commit -m "cd workflow"`
`git push origin master`

### 3. Publish NPM Packages

Inside the repo: `.github/workflows/package.yml`

````
name: Sveltefire Package

on:
    release:
        types: [created]

jobs:
    build:

    publish-npm:
        needs: build

    publish-gpr:
        needs: build
````

### 4. Integrate Apps

**Actions** are reusable chunks of code for your own workflows
**Apps** are fully-managed integrations

Inside the repo: `.github/workflows/slack.yml`

````
name: Slack Issues

on:
    issues:
        types: [opened]

jobs:
    post_slack_message:
        runs-on: ubuntu-latest
        steps:
            - uses: rtCamp/action-slack-notify@v2.0.0
        env:
            SLACK_WEBHOOK: ${{ secret.SLACK_WEBHOOK }}
            SLACK_USERNAME: CyberJess
            SLACK_CHANNEL: gh-issues
````

### 5. Schedule Background Jobs

Inside the repo: `.github/workflows/package.yml`

````
name: Export Firestore Data

on:
    schedule:
        - cron: '0 0 * * *'
        steps:
        - uses: GoogleCloudPlayform/github-actions/setup-gcloud@master
            with:
                service_account_key: ${{ secret.GCP_SA_KEY }}
                export_default_credentials: true
            - run: gcloud config set project $PROJECT_ID
            - run: gcloud firestore export $BUCKET
````

- [GitHub Action deploying Angular App to Firebase Hosting](https://fireship.io/snippets/github-actions-deploy-angular-to-firebase-hosting/)
- [Demo Code](https://github.com/fireship-io/225-github-actions-demo)
- [Github Actions](https://github.com/features/actions)
