Clone your forked `minerva` repository and work on files locally or perform below steps in http://github.com UI.
Documentation files are located under `service/docu/files/` directory.

### Create new documentation file called `details.html.md`
* It should contain the following metadata:
```
---
title: 'Full Story'
type: 'Details'
service: 'Minerva'
---
```
* Content part should contain explanation of what the service is about. Consult with current documentation.
Few hints:
 - Write about the benefits
 - Write about the background -> service inspired by [Sarah Maddox idea](https://ffeathers.wordpress.com/)
 - Write about potential usage

### Save and publish

1. Save changes. In case you are using Git CLI it means commit and push them to the `minerva` repository.
2. Make sure they are visible on your documentation Web Page created using previous workshop steps.
```
Run below command in terminal where your docpad-skeleton-apidocs repository is located
> npm run init
> NODE_ENV=prod npm run compile
> npm run preparePushResult && npm run pushResult
```

### See your changes on production

Open in the browser the following link: http://your_github_username.github.io and notice your updated documentation
