## USGS Citations Project

This project uses the Python package called [habanero](https://habanero.readthedocs.io/en/latest/modules/crossref.html) to query the [CrossRef Database API](https://github.com/CrossRef/rest-api-doc) for information on USGS DOIs for data releases and the package called [pprintjson](https://github.com/clarketm/pprintjson) for easy viewing of the query results. 

These packages can easily be installed using `pip install habanero` and `pip install pprintjson`. 

USGS has a spreadsheet that contains the data release DOI (column called dr_doi) and the DOI for the publication associated with the data release (column called rel_pub_url). 

One goal is to auto-populate the spreadsheet with the following information about the rel_pub_url:
* title
* journal name
* year of publication
* publisher

However, the primary goal is to identify whether the data release doi (dr_doi) is actually cited within the publication (rel_pub_url), and if so, document where it is cited (e.g. references section, main text body, figure caption). 

Searching of the references can be completed with habanero for those publications that have a reference list available in CrossRef. 

Per the Habanero documentation on the CrossRef API: 
> When you search with query terms, on Crossref servers, it will not search full text, or even abstracts of articles, but only what is available in the API data response options. That is, it searches titles, authors, year of publication, reference list (if one is available), etc. For some discussion on this, see https://github.com/CrossRef/rest-api-doc/issues/101

```python

```
