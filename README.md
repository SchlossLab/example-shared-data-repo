# example-shared-data-repo

this is an example of how to share a directory with large data that is always up to date

The data directory is actually a symbolic link to a location on axiom that will store all our big data files. You can use the repo data directory in your scripts just as if the large data files were in your repo. Any updates to the data directory will be instantly available to anyone who's using the linked directory.
