# Webforms / Entity Forms

## Survey Forms

- Collect info
- Provide feedback
- Event registration
- Application forms

Not considered to be website content.

### Solutions
Form API...a lot of work.
Content type with exposed fields/permissions -- not good!
Embed 3rd party.

### Survey form modules

- Allow results to be processed.
- Store submissions for futher analysis.
- Support notification for admins and users
- Access control.

_Webform vs EntityForm_

## Webform

- Created in 2004
- More than 450k installations
- Almost 150 releases since Drupal 4.4.x
- _defacto_ standard
- Does not use FORM API

## EntityForm
- 2011
- 15k installations
- Created for D7 based on its architecture.
- Req. views
- Integrates better with other modules.

Webform is more scalable for sites with many and/or big forms.

Entityform - Multipage can use field-group module.

## Deployment
Webform was created 11 years ago. Hard to deploy.
EntityForms can be exported and deployed. Using Features.
Webforms are a bitch to deploy. UUID/node-export is unreliable.

## Questions to help decide
- How many forms will be necessary?
- How many fields per form will be necessary?
- Will the site be multilingual?
- Will the form admins be familiar with Drupal?
- What kind of field types?
- How dynamic will the fomrs be?

## Example - Course Feedback Site

Login to site, create courses and then create form - End User form creation.
