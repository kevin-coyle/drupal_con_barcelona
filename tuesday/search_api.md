# Search Api
_Thomas Seidl_

Live demo of search API in D8.

- Created in 2010, for D7
- Improved core search.

Need to enable:
- Search API
- Database Search Module (Solr Available)

>*Disable Search Module* in core.

You can add multiple servers, and vary the backend.

Configurable by bundles.

Select server and add a descriptions. You can index items immediately in the advanced options.

## Index items immediately

### Pro:
- No stale data
  - Security Concerns
- User experience

### Con:
- Performance
- Possibly longer waits

Usually a good idea to do this on smaller sites. Not so great for large sites.

---
Select fields that it wants to index. Can select weight and data type.

String means one keyword or name, like the content type which can be a few strings.

Full text splits individual words which can be found.

## Processors

Aggregated fields add additional fields.

### Access Control

Implemented drupals own access control. Otherwise need manual control.

## Creating the search

Use views to create the search. Only way included in search API.

## Search with Solr.

Basically works. Not yet ready
1. Enable solr search module.
2. Install module deps with composer. (Uses solarium)
3. Get a working solr server.
4. Copy drupal configuration into solr dir.
5. Start server.

For docker [Official Docker](https://github.com/makuk66/docker-solr)

No need to install tomcat anymore :D yay.

1. Create a new core in solr admin gui. (must be a way to script this). Or just use the docker command.

Addons:

- Facets - a long way from being done.
- Autocomplete
- Saved Searches
