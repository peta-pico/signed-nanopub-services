Signed Nanopub Services
=======================

This is a variation of the [Nanopub Services](https://github.com/peta-pico/nanopub-services.git)
focussing on the signed nanopublications.

The nanopub server of this set of services replicates all published
nanopublications, but the grlc and LDF services only cover the signed ones.
On top of that and in contrast to the plain Nanopub Services, here also
the Virtuoso triple store is made available via SPARQL.


## Pre-Packaged Data

    $ wget https://zenodo.org/record/5888258/files/mongodb0.tar.gz
    $ tar -xvzf mongodb0.tar.gz && rm mongodb0.tar.gz

    $ wget https://zenodo.org/record/5888258/files/signed-virtuoso.tar.gz
    $ tar -xvzf signed-virtuoso.tar.gz && rm signed-virtuoso.tar.gz


## Services

### Nanopub Server

A service to publish and individually retrieve nanopublications.

<h3 id="grlc-np-api">grlc Signed Nanopub API</h3>

The [grlc](https://grlc.io)-based [nanopub-api](https://github.com/peta-pico/nanopub-api)
running on all the signed nanopublications.

<h3 id="np-ldf-server">Signed Nanopub LDF Server</h3>

A service providing [Linked Data Fragments (LDF)](https://linkeddatafragments.org/) access
to all the signed nanopublications.

<h3 id="np-sparql-api">Signed Nanopub SPARQL API</h3>

A service providing SPARQL access to all the signed nanopublications.

