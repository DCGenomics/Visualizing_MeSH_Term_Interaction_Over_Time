# MeSHgram
<b>A tool to visually browse co-occurrence of MeSH terms in PubMeb.</b>

Publications indexed in PubMed have human curated MeSH terms associated with them.
We leverage these MeSH terms and create a visual search tool to find articles in PubMed.
The idea is that a visual inspection of co-occurrences is helpful for exploratory queries to PubMed.

## Software Artifacts

Server code was tested in Python 3.5 and Web client was tested in all major browsers except FireFox.

<b>url_gen.py</b> - generates Pubmed XML archive urls to be fed to wget to download.

<b>pm2mdb.py</b> - parses the downloaded Pubmed XML archives and loads them into Mongodb.

<b>server.py</b> - CherryPy based server that provides json end points for the Web Front End.

<b>config.txt</b> - CherryPy config file.

<b>terms.txt</b> - list of all MeSH terms, alphabetically sorted, extracted from the database.

<b>mesh_stopwords.txt</b> - "Stop words" among MeSH terms. We calculated the 100 most frequent MeSH terms across the entire corpus and manually curated some terms out.

