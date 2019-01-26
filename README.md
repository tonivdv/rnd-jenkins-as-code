Jenkins CasC Runnable Demo
--------------------------

## Prerequisites

- Docker

## Run

One of the jcasc configurations (casc_configs/bitbucket-oauth.yaml) configures jenkins to authenticate using Bitbucket OAuth. In order to make this work, you must add a consumer for your Jenkins instance. Follow the instructions on the "Bitbucket OAuth" plugin at https://plugins.jenkins.io/bitbucket-oauth . The "callback url" to use depends on the url of your Jenkins server, and highly depends on how you use docker on your machine.

Once you have your client_id and secret, copy `secrets/bitbucket_oauth_client_id.dist` to `secrets/bitbucket_oauth_client_id` and `secrets/bitbucket_oauth_secret.dist` to `secrets/bitbucket_oauth_secret` and copy the value accordingly in the file.

```
  docker-compose up -d
```

If you make changes to the dockerfile you must rebuild your docker image by doing:

```
  docker-compose build --pull
```
