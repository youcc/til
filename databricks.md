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


