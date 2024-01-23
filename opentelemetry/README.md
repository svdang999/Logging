### Ref
```
https://opentelemetry.io/docs/kubernetes/helm/collector/
```

### Deploy example
```
root@HNCWIN11:~# helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts
"open-telemetry" has been added to your repositories
root@HNCWIN11:~# helm repo update
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "open-telemetry" chart repository
...Successfully got an update from the "camunda" chart repository
...Successfully got an update from the "ingress-nginx" chart repository
...Successfully got an update from the "stable" chart repository
...Successfully got an update from the "kong" chart repository
...Successfully got an update from the "falcosecurity" chart repository
...Successfully got an update from the "azure-marketplace" chart repository
...Successfully got an update from the "prometheus-community" chart repository
Update Complete. ⎈Happy Helming!⎈
root@HNCWIN11:~# helm -n open-telemetry-infra-dev install ol-infra-dev open-telemetry/opentelemetry-collector --set mode=deployment -f https://raw.githubusercontent.com/svdang999/Logging/main/opentelemetry/opentelemetry-collector-values.yaml
NAME: ol-infra-dev
LAST DEPLOYED: Tue Jan 23 16:07:40 2024
NAMESPACE: open-telemetry-infra-dev
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
[WARNING] No resource limits or requests were set. Consider setter resource requests and limits for your collector(s) via the `resources` field.

[WARNING] "useGOMEMLIMIT" is enabled but memory limits have not been supplied, which means no GOMEMLIMIT env var was configured but the Memory Ballast Extension was removed. It is highly recommended to only use "useGOMEMLIMIT" when memory limits have been set.
```
