# pod_readiness_gate

Source: [base/pkg/kusion_kubernetes/api/core/v1/pod_readiness_gate.k](https://github.com/KusionStack/konfig/tree/main//base/pkg/kusion_kubernetes/api/core/v1/pod_readiness_gate.k)

This is the pod\_readiness\_gate module in kusion\_kubernetes.api.core.v1 package.<br />This file was generated by the KCL auto-gen tool. DO NOT EDIT.<br />Editing this file might prove futile when you re-run the KCL auto-gen generate command.

## Schema PodReadinessGate

PodReadinessGate contains the reference to a pod condition

### Attributes

|Name and Description|Type|Default Value|Required|
|--------------------|----|-------------|--------|
|**conditionType**<br />ConditionType refers to a condition in the pod's condition list with matching type.|str|Undefined|**required**|
<!-- Auto generated by kcl-doc tool, please do not edit. -->