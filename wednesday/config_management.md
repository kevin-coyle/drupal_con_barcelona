# Configuration Management in D8

## Why config management

- Deployment
- Predictable - known robust.

Difficult with cTools and Features still....
`variable_get()` still required default set everywhere. Hard to maintain.

## What is config management

Configuration is not:
- state
- cache
- content (nodes, taxonomy, users)

Configuration is:
- everything that is left

A place to store that you'd like to sync between dev and prod.

## Using configuration

````
$site_name = \Drupal::config('system.site')
  ->get('name')
````
## Creating configuration

For the file module:
- yml file in `file/config/install/file.settings.yml` single instance of config.
- views - `file/config/optional/views.view.files.yml` only makes sense if views installed.

### file.settings.yml

````
description:
  type: 'textfield'
````

etc....

## Through the API

Get editable ver of the configFactory()

````
$config = \Drupal::configFactory()->getEditable();
````

## Configuration entities

Relations between entities are now important for deployment.
Uninstalls now include configuration. :)

## Config entities deps

- Modules
- Themes
- Other Config entities
- Content

e.g Roles dep on user module. 
