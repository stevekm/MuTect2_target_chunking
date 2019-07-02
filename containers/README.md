Build Docker and Singularit containers. Building Singularity containers requires Vagrant installation. 

Build Docker container:

```
make docker-build VAR=dirname
```

Test Docker container:

```
make docker-test VAR=dirname
```

Build Singularity container:

```
make singularity-build VAR=dirname
```

Test Singularit container:

```
make singularity-test VAR=dirname
```
