# Tips and Tricks to work with helm charts

### Deleting all charts from a namespace

```shell
export NAMESPACE='default'
helm delete --purge $( helm ls --all | grep -i deployed | grep ${NAMESPACE} | awk {'print $1'})
```
