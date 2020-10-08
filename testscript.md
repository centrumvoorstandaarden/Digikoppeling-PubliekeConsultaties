git-tag - Create, list, delete or verify a tag object signed with GPG

get the latest tags from repository

```
git fetch --tags
```

git-rev-list - Lists commit objects in reverse chronological order

get the latest commit

```
$temp2 = git rev-list --tags --max-count=1
```

git-describe - Give an object a human readable name based on an available ref

find the most recent tag that is reachable from a commit

```
$temp = git describe --tags $temp2
```

git-checkout - Switch branches or restore working tree files

get the latest tagged commit
```
git checkout $temp
```

Dus als script gecombineerd wordt uitgevoerd
```
git fetch --tags
$temp2 = git rev-list --tags --max-count=1
$temp = git describe --tags $temp2
git checkout $temp
```

dan wordt de laatste tagged version opgehaald (en dus niet de laatste commit)



source: <https://devconnected.com/how-to-checkout-git-tags/>