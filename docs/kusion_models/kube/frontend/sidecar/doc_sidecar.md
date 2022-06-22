# sidecar

Source: [base/pkg/kusion_models/kube/frontend/sidecar/sidecar.k](https://github.com/KusionStack/konfig/tree/main//base/pkg/kusion_models/kube/frontend/sidecar/sidecar.k)

## Schema Sidecar

Sidecar describes the sidecar container configuration that is expected to be run on the host.

### Attributes

|Name and Description|Type|Default Value|Required|
|--------------------|----|-------------|--------|
|**name**<br />A Container-level attribute.<br />The container name. Each container in a pod must have a unique name.|str|Undefined|**required**|
|**command**<br />A Container-level attribute.<br />The startup command of main process. The image's entrypoint is used if this is not provided.|[str]|Undefined|optional|
|**args**<br />A Container-level attribute.<br />The startup arguments of main process. The image's cmd is used if this is not provided.|[str]|Undefined|optional|
|**env**<br />A Container-level attribute.<br />List of environment variables in the container.|[[env.Env](../container/env/doc_env.md#schema-env)]|Undefined|optional|
|**envFrom**<br />A Container-level attribute.<br />List of sources to populate environment variables in the container.|[[env.EnvFromSource](../container/env/doc_env.md#schema-envfromsource)]|Undefined|optional|
|**ports**|[[port.ContainerPort](../container/port/doc_container_port.md#schema-containerport)]|Undefined|optional|
|**resource**<br />A Pod-level attribute.<br />Sidecar container resource. |str \| [resource.Resource](../resource/doc_resource.md#schema-resource)|"1<cpu<2,1Gi<memory<2Gi,disk=20Gi"|**required**|
|**image**<br />A Container-level attribute.<br />Docker image name. More info: https://kubernetes.io/docs/concepts/containers/images|str|Undefined|**required**|
|**readinessProbe**<br />A Container-level attribute.<br />The probe to check whether container is ready or not.|[p.Probe](../container/probe/doc_probe.md#schema-probe)|Undefined|optional|
|**livenessProbe**<br />A Container-level attribute.<br />The probe to check whether container is live or not.|[p.Probe](../container/probe/doc_probe.md#schema-probe)|Undefined|optional|
|**startupProbe**<br />A Container-level attribute.<br />The probe to indicates that the Pod has successfully initialized.|[p.Probe](../container/probe/doc_probe.md#schema-probe)|Undefined|optional|
|**lifecycle**<br />Actions that the management system should take in response to container lifecycle events.<br />Cannot be updated.|[lc.Lifecycle](../container/lifecycle/doc_lifecycle.md#schema-lifecycle)|Undefined|optional|
|**workingDir**<br />Container's working directory. If not specified, the container runtime's default will be used, <br />which might be configured in the container image. Cannot be updated.|str|Undefined|optional|
|**securityContext**<br />SecurityContext defines the security options the container should be run with.<br />If set, the fields of SecurityContext override the equivalent fields of PodSecurityContext.<br />More info: https://kubernetes.io/docs/tasks/configure-pod-container/security-context/|{str: any}|Undefined|optional|
### Examples
```python
import base.pkg.kusion_models.kube.frontend.sidecar as s
import base.pkg.kusion_models.kube.frontend.container.probe as p

sidecar = s.Sidecar {
    name = "test"
    livenessProbe = p.Probe {
        handler = p.Http {
            httpPath = "/healthz"
        }
        initialDelaySeconds = 10
    }
}
```

<!-- Auto generated by kcl-doc tool, please do not edit. -->