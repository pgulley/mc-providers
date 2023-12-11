Media Cloud Providers Library
=============================

A package of search providers for Media Cloud, wrapping up interfaces for different social media platform.

UNDER CONSTRUCTION- Probably won't get a huge amount of attention for a little bit, but I'm putting this 
up now since I've done this extraction already.

Install with pip (`pip install .`) and the `install.sh` script. 

Requires environment variables set for various interfaces to work correctly.


### Build

Make sure `pip install flit twine` so you can build and deploy to PyPI.

1. Bump the version number in `pyproject.toml`
2. Run `flit build` to create an installation package
3. Add a note about changes to the version history below
4. Commit the changes and tag it with a semantic version number
5. Run `twine upload --repository-url https://test.pypi.org/legacy/ dist/*` to upload it to PyPI's test platform
6. Run `twine upload dist/*` to upload it to PyPI

### Version History
* __v0.4.0__ - Specify custom base URLs via new string param to `provider_by_name` and `provider_for` 
* __v0.3.0__ - Add support for paging through stories directly, and including text in paged results for speed
* __v0.2.6__ - Fixed querying by domain on new mediacloud system
* __v0.2.5__ - Alignment with new mediacloud system. Old onlinenews provider is now "onlinenews-mclegacy", "onlinenews-mediacloud" now queries the new index.
* __v0.2.4__ - Added support for api keys via "provider_by_name"
* __v0.2.3__ - removed support for API keys in environment variables- now expected as an argument in `providers.provider_for`
* __v0.2.2__ - transition to use the dedicated mediacloud-api-legacy package to avoid version conflictsgit
* __v0.2.1__ - add in a date hack to resolve a lower-level bug in the Media Cloud legacy count-over-time results
* __v0.2.0__ - add in support for Media Cloud legacy database
* __v0.1.7__ - corrected support for a "filters" kwarg in online_news
* __v0.1.6__ - Added support for a "filters" kwarg in online_news
* __v0.1.5__ - Added politeness wait to all chunked queries in twitter provider
* __v0.1.4__ - Added Query Chunking for large collections in the Twitter provider
* __v0.1.3__ - Added Query Chunking for large queries in the onlinenews provider
* __v0.1.2__ - Test Completeness
* __v0.1.1__ - Parity with web-search module, and language model
* __v0.1.0__ - Initial pypi upload 
