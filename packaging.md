Packaging DBs
=============

See also [this](https://github.com/peta-pico/nanopub-services/blob/master/packaging.md).


## Resetting password in signed-virtuoso

Extract in empty directory:

    $ tar -xvzf signed-virtuoso.tar.gz && rm signed-virtuoso.tar.gz

Run virtuoso container:

    $ docker run -v $(pwd)/data/virtuoso:/data -d nanopub/virtuoso

Execute shell in container:

    $ docker exec -it $(docker ps -q --filter ancestor=nanopub/virtuoso) sh

Reset password in container (replace "PASSWORD" with actual password):

    # echo "user_set_password('dba', 'dba');\nexit;" | isql-v -U dba -P PASSWORD
    # exit

Stopping virtuoso:

    $ docker stop $(docker ps -q --filter ancestor=nanopub/virtuoso)

Create new zip file:

    $ tar --exclude=data/virtuoso/virtuoso.log --exclude=data/virtuoso/dumps --exclude=data/virtuoso/virtuoso.trx --exclude=data/virtuoso/.dba_pwd_set -czvf signed-virtuoso0.tar.gz data/virtuoso

