# Expose Drupal with RESTful
_Mateu Aguilo_

This is mainly D7.

Rest is more than just exporting entities.
 - CRUD, Auth, filtering

Benefits:
  - Data providers
  - Resource composition (Resource Nesting)
    - Entity that relates another entity. Stop multiple reqs.
  - URL query language.

API is a contract between backend team and front end team. You could remove Drupal and put something in its place.

*Avoid Drupal leaking into your Design*

No und, nid....etc

<table>
  <tr>
    <th>Drupal specific design</th>
    <th>Generic Design</th>
  </tr>
  <tr>
    <td>`node/{nid}`</td>
    <td>`restaurant/{{uuid}}, deal{{uuid}}`</td>
  </tr>
  <tr>
    <td>`description: {
      'und': {
        'value': '123'
      }
      } `</td>
    <td>`description: 123`</td>
  </tr>
</table>

### Version your API

Always make sure that the api have a version number, even if you think it won't need it.

- Can be used for rollbacks too. Keep it in version control.
- Deploy multiple versions of the API simultaneously.
- Allow you to release it for the world and increase stability.

## Features
- Developer Orientated - 100% Features Module Free
- Everything is in CTools plugins

## How to create a resource.

<!-- @todo add image of plugin -->
1. Create a class with an annotation.
2. Map fields in the `publicFields()` method.
