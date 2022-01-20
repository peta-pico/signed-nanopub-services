Signed Nanopub Services
=======================

This is a variation of the [Nanopub Services](https://github.com/peta-pico/nanopub-services.git)
focussing on the signed nanopublications.

The nanopub server of this set of services replicates all published
nanopublications, but the grlc and LDF services only cover the signed ones.
On top of that and in contrast to the plain Nanopub Services, here also
the Virtuoso triple store is made available via SPARQL.


## Services

### Nanopub Server

A service to publish and individually retrieve nanopublications.

<h3 id="grlc-np-api">grlc Nanopub API</h3>

The [grlc](https://grlc.io)-based [nanopub-api](https://github.com/peta-pico/nanopub-api)
running on all the signed nanopublications.

<h3 id="np-ldf-server">Nanopub LDF Server</h3>

A service providing [Linked Data Fragments (LDF)](https://linkeddatafragments.org/) access
to all the signed nanopublications.

