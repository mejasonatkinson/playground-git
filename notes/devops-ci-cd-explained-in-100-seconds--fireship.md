# [DevOps CI/CD Explained in 100 Seconds; Fireship](https://www.youtube.com/watch?v=scEDHsr3APg)

Continuous Integration (CI)

Commit code to a shared repo frequently

GitHub Actions

````
name: CI/CD is Easy!

on:
    push:
        branches:
            - master
jobs:
    build:
        runs-on: ubuntu-latest

    steps:
        - uses: actions/checkout@v2
        - uses: actions/setup-node@v1
          with:
            node-version: 12
        - run: npm ci
        - run: npm test
        - run: npm run build
        - run: npm run deploy
````

Helps automate things.

Helps spot problems early, before they become bigger issues.