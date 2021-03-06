## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: authoring
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: authoring_2_0
```

### Tag: authoring_2_0 and go

These settings apply only when `--tag=authoring_2_0 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'authoring_2_0' && $(go)
output-folder: $(go-sdk-folder)/services/cognitiveservices/v2.0/luis/$(namespace)
```