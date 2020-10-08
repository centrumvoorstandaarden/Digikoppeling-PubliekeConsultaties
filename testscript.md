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

source: <https://devconnected.com/how-to-checkout-git-tags/>