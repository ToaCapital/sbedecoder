## How to deploy to Nexus

```shell
python -m build  
```

```shell
twine upload --repository nexus dist/* 
```

Assumes you have a `~/.pypirc` file with the following contents:

```shell
[distutils]
index-servers =
    nexus
    
[nexus]
repository: https://<username>@build.mfx.mahimarkets.com/nexus/repository/mahi-python/

```

