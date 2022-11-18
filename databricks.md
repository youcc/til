# Install databricks-connect in Unix/Linux
### supposed you already installed WSL on your Windows

## Install Java sE Runtime
[Installing Oracle JRE on Ubuntu](https://ubuntu.com/tutorials/install-jre#3-installing-oracle-jre)

## Install Databricks Connect client
```
pip3 install -U databricks-connect==7.3.*  # match your cluster version
```

## Configure connection properties
```
databricks-connect configure
```

## lateral view

- what is `lateral view`
  - can be used to `explode` duplicated arrays by a key in order to group distinct values
  - good for less code
    - instead of `select key, collect_list(item) from (select explode(array) as item from table) group by key`
    - it becomes `select key, collect_list(item) from table lateral view explode(array) group by key`
- a gotcha when doing this
  - if the `array` used is `null` then the `lateral view explode(array)` actually acts a filter and removes rows that have a `null` `array`  so for the `group by` there would be less output rows

