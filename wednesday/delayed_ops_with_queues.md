# Delayed operations with queues
_Frederic G. Marand_

## Why use queues?

- Faster for visitors and editors.

## Use cases

- Non Drupal front ends
- Anticipate content generation
- Deferred submits
- Slow ops, node saves, previews etc
- External data sources
- Multi-step ops.
- Batch ops.


Drupal generates content -> queue -> redis -> Front End

At no point does the user exp. any lag. Front end will serve previous version.

## Anticipating generation

### Usual

Fresh        |         stale          |         Expired
---                   ---                     ---
Content created  ->  served from cache  ->  regenerate cache.


### Anticipated content generation.

Created content  -> Served from cache -> req. update ^ store


This stops one unlucky user from getting a *CACHE MISS*

- Heavy processes.


## Job servers

- How to get results
- Rerun filed jobs
- Separated queue for failed jobs
- Monitoring queues, workers.
- Supervisor - deamon native for UNIX systems.

Available in D7 for mongodb, memory, database, SQS, Beanstalkd
