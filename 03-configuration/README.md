# Creating ConfigMaps in different ways

There are 3 ways of creating a ConfigMap

### Literal values

```
$ kubectl create configmap db-config \
  --from-literal=db_name=ecommerce \
  --from-literal=db_port=3000
```

### Single file with environment variables

```
$ kubectl create cm db-config-env --from-env-file=db-config.env
```

### Single file

```
$ kubectl create cm db-config-file --from-file=db-config.txt
```

# Creating Secret

### Literal values

```
$ kubectl create secret generic db-creds --from-literal=pwd=s3cr3!
```

### Single file

```
$ kubectl create secret genetic db-creds --from-file=db-config.txt
```
