# Run End-to-End Tests

Install [Sonobuoy](https://github.com/vmware-tanzu/sonobuoy)

```
wget https://github.com/vmware-tanzu/sonobuoy/releases/download/v0.18.4/sonobuoy_0.18.4_linux_amd64.tar.gz

sudo tar -zxvf sonobuoy_0.18.4_linux_amd64.tar.gz
sudo mv sonobuoy /usr/local/bin
```

## Run CNCF sonobuoy tests 

```
sonobuoy run --wait
```

> Note: This may take additional resources for your workers in my case it required 4Gb RAM and 2 CPU which I was added manually

This could take about 1.5 to 2 hours. The number of tests run and passed will be displayed at the end.

## See results

Get the results from the plugins (e.g. e2e test results):

```
results=$(sonobuoy retrieve)
```

Inspect results for test failures. This will list the number of tests failed and their names:

```
sonobuoy results $results
```

Deleting Sonobuoy entails removing its namespace as well as a few cluster scoped resources.

```
sonobuoy delete --all --wait
```
