# Link a submodule to a git repository

Reference: [How can I have linked dependencies in a git repo?](https://stackoverflow.com/questions/7813030/how-can-i-have-linked-dependencies-in-a-git-repo)

Use the command git submodule

```
git submodule add path_to_repo path_where_you_want_it
```

## Example

### Add submodules to git repository

At the top level of the git repository:

```
git submodule add git://github.com/example/some_lib.git lib/some_lib
```
After adding a submodule, or when doing a fresh checkout of the repository:

```
git submodule init
git submodule update
```

### Update submodules in git repository

To update to a newer version of one of the libraries, cd into the submodule and pull.

```
cd lib/some_lib
git pull
```

Commit the update.

```
git status
git add lib/some_lib
git commit -c "update some lib"
```

Collaborators will see lib/some_lib as modified until they do:

```
git submodule update
```

***
*Updated on 23 December 2025*
