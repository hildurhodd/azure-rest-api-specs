## Python

These settings apply only when `--python --track2` is specified on the command line.
Please also specify `--python-sdks-folder=<path to the root directory of your azure-sdk-for-python clone>`.

``` yaml $(python) && $(track2)
azure-arm: true
license-header: MICROSOFT_MIT_NO_VERSION
namespace: azure.mgmt.netapp
package-name: azure-mgmt-netapp
package-version: 1.0.0b1
clear-output-folder: true
no-namespace-folders: true
```

### Python multi-api

``` yaml $(python) && $(multiapi) && $(track2)
clear-output-folder: true
python-mode: create
batch:
  - tag: package-netapp-2021-08-01
  - tag: package-netapp-2021-06-01
  - tag: package-netapp-2021-04-01
  - tag: package-netapp-2021-02-01
  - multiapiscript: true
```

``` yaml $(multiapiscript)
output-folder: $(python-sdks-folder)/netapp/azure-mgmt-netapp/azure/mgmt/netapp/
clear-output-folder: false
perform-load: false
```

### Tag: package-netapp-2021-08-01 and python

These settings apply only when `--tag=package-netapp-2021-08-01 --python` is specified on the command line.

``` yaml $(tag) == 'package-netapp-2021-08-01' && $(python) && $(track2)
namespace: azure.mgmt.netapp.2021-08-01
output-folder: $(python-sdks-folder)/netapp/azure-mgmt-netapp/azure/mgmt/netapp/2021-08-01
```

### Tag: package-netapp-2021-06-01 and python

These settings apply only when `--tag=package-netapp-2021-06-01 --python` is specified on the command line.

``` yaml $(tag) == 'package-netapp-2021-06-01' && $(python) && $(track2)
namespace: azure.mgmt.netapp.2021-06-01
output-folder: $(python-sdks-folder)/netapp/azure-mgmt-netapp/azure/mgmt/netapp/2021-06-01
```

### Tag: package-netapp-2021-04-01 and python

These settings apply only when `--tag=package-netapp-2021-04-01 --python` is specified on the command line.

``` yaml $(tag) == 'package-netapp-2021-04-01' && $(python) && $(track2)
namespace: azure.mgmt.netapp.2021-04-01
output-folder: $(python-sdks-folder)/netapp/azure-mgmt-netapp/azure/mgmt/netapp/2021-04-01
```

### Tag: package-netapp-2021-02-01 and python

These settings apply only when `--tag=package-netapp-2021-02-01 --python` is specified on the command line.

``` yaml $(tag) == 'package-netapp-2021-02-01' && $(python) && $(track2)
namespace: azure.mgmt.netapp.2021-02-01
output-folder: $(python-sdks-folder)/netapp/azure-mgmt-netapp/azure/mgmt/netapp/2021-02-01
```