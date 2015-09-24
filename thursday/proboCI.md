# Probo CI
Another CI tool.

## Trad work flow

Make ticket -> code -> commit -> Review on Dev

## Better workflow

Make ticket -> code -> commit to feature branch -> review branch & merge to dev

---
Many tickets merged together into one dev env. Can be Difficult after client review if they make amends.

## Probo.CI

- Open Source CI
- SAAS

## New workflow

Make ticket -> code -> pull req -> client review -> lead deploys

### Without Probo

- Master has mix of things that are not vetted by clients
- Testing feature branches is hard. Devs work on master
- Only devs can see anything on a feature branch

### With Probo
- Master ready to deploy

## How its done

Written in nodeJS & docker. Runs fat containers.

### Nginx

- Terminate SSL
- Routes to microservice

### Github
- Rec webhooks
- Gets `probo.yml`

### Container Manager
- Drives Docker
- Starts/Stops Containers

http://probo.ci/bcn Invite for demo
