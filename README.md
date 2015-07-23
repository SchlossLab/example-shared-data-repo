# example-shared-data-repo

this is an example of how to share a directory with large data that is always up to date

The data directory is actually a symbolic link to a location on axiom that will store all our big data files. You can use the repo data directory in your scripts just as if the large data files were in your repo. Any updates to the data directory will be instantly available to anyone who's using the linked directory.

If you want to completely undermine the entire point of the linked data directory, for example if you have the data locally, you can ignore changes to the data directory and then re-assign the symlink locally:

```bash
git update-index --assume-unchanged data
ln -sf /Users/kiverson/testdata data
```

where `/Users/kiverson/testdata` is your local data directory. Note: this WILL NOT be tracked and other users of the repo will not see any changes you make to data/.

If you plan to work this way you'll want to put the data directory in your local git exclude `.git/info/exclude` and  this will exclude the data diretory from being tracked on your local machine but won't affect other users.
