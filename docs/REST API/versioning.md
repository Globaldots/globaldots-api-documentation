# Versioning
The API is versioned, and the version is part of the URL.

## Versions
2017-05-01	v1


## Breaking Changes

Not all API changes will trigger a new version. Specifically new items can be added to endpoints without changing the version. Because of this, your app should not rely on there only being certain items in the json of a response.

Any change that removes something from the result, or changes the format of data will normally be made in a new version.