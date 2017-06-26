# MailingListParser

[![Build Status](https://travis-ci.org/prasadtalasila/MailingListParser.svg?branch=development)](https://travis-ci.org/prasadtalasila/MailingListParser) 
[![Code Climate](https://codeclimate.com/github/prasadtalasila/MailingListParser/badges/gpa.svg)](https://codeclimate.com/github/prasadtalasila/MailingListParser) [![Requirements Status](https://requires.io/github/prasadtalasila/MailingListParser/requirements.svg?branch=development)](https://requires.io/github/prasadtalasila/MailingListParser/requirements/?branch=development)


> Parsing mailing lists to detect communication patterns.

Welcome to the MailingListParser project! The main objective of this project is to develop a mailing list parser to extract information from a mailing list such as senders,receivers, time stamps etc and then use this to construct an organizational (or communication) structure like conversation thread hypergraphs for further analysis. We utilize social network analysis techniques to examine the relationships between authors on common mailing lists like LKML, Sakai etc. Study of these interactions on different levels helps us in deriving the local and global communication patterns between users on different threads. THis project draws its inspiration from various fields such as data mining, graph theory, information retrieval and inferential modelling in order to form predictive models that help in understanding certain intricate characteristics of a social network. This involves analyzing graphs with, say, authors as nodes and their correspondences as edges, to study the details about various network graph properties such as density, size, node centrality, degree, connectedness etc.

![Vertex Clustering](https://github.com/prasadtalasila/MailingListParser/blob/master/data/lkml/graphs/vertex_clustering_infomap.png)

## Usage

The library's working has been modularised into many modules namely data_handling, author_analysis amd thread_analysis. The [test_driver.py file](https://github.com/prasadtalasila/MailingListParser/blob/development/lib/test_driver.py) presents a brief overview of how one can use IRCLogParser for parsing and analysis.

Some of the visualisable sample outputs can be seen [here](https://github.com/prasadtalasila/MailingListParser/tree/development/data), categorized into various datasets, giving an idea about this project's capabilites and as to what kind of insights we can and we plan to derive from the datasets.

## Documentation

MailingListParser uses [Sphinx Python Documentation Genertor](http://www.sphinx-doc.org/en/stable/) for generating documentation of the library. The documentation is setup to work with [Google Style Docstrings](http://www.sphinx-doc.org/en/stable/ext/example_google.html) which eases the documentation writing process.

The documentation is deployed on the branch `gh-pages` who's updation has been made automatic by the a bash script which otherwise requires to run `make html` in docs directory after every commit.

You can view the documentation hosted on `gh-pages` [here](http://prasadtalasila.github.io/MailingListParser/).

## Testing Framework

Presently, MailingListParser has various end-to-end implemented which reside in the [test directory](https://github.com/prasadtalasila/MailingListParser/tree/development/test/). We use py.test as the unit test framework and you can get a comprehensive idea of the various use cases of each of the modules from the corresponding tests.

## Installation

MailingListParser depends on various third-party libraries which are listed in [requirements.txt](https://github.com/prasadtalasila/MailingListParser/blob/development/requirements.txt). 
Run `pip install -r requirements.txt` in the root directory to install these dependencies.

## License

IRCLogParser is available under the [MIT License](https://github.com/prasadtalasila/IRCLogParser/tree/master/LISENCE.txt)
