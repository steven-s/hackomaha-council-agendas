# hackomaha-council-agendas
***

**City Council Agendas**

# Installation
***

- Git clone this
- Run install/install.sh to install the project dependencies.
- You will also need to have an [elasticsearch](http://www.elasticsearch.org) database installed and running at `http://{host}:9200/citycouncil`


# Hot Search Terms
***
- Zoning / Zone / Rezone
- Liquor / "Special Designated License"
- Planning
- Public Hearing
- Annex / Subdivision
- OPW
- Mayor
- CSO
- Contract / Purchase Order / Interlocal / Processional Service Agreement

# Sub-Projects
***

## agendastojson/bin/agendastojson
***
1. Grabs all pdf's on the agenda page and stores them to `data/` in the current working directory
2. Converts all the pdf's to text
3. Posts the pdf's to the elasticsearch server
4. Cleans up after itself

## elasticsearch
***

[elasticsearch](http://www.elasticsearch.org) is an "open source, distributed, RESTful search engine." It is used as the search database for the agendas and their extracted metadata.  Individual agendas are identified by their date.

To access a specific agenda by its identifier, use the URL format:
`http://simomaha.com:9200/citycouncil/agendas/{dashed-date}`

example:
[http://simomaha.com:9200/citycouncil/agendas/2012-10-16](http://simomaha.com:9200/citycouncil/agendas/2012-10-16)

