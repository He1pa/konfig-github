# rolling_update_stateful_set_strategy

Source: [base/pkg/kusion_kubernetes/api/apps/v1/rolling_update_stateful_set_strategy.k](https://github.com/KusionStack/konfig/tree/main//base/pkg/kusion_kubernetes/api/apps/v1/rolling_update_stateful_set_strategy.k)

This is the rolling\_update\_stateful\_set\_strategy module in kusion\_kubernetes.api.apps.v1 package.<br />This file was generated by the KCL auto-gen tool. DO NOT EDIT.<br />Editing this file might prove futile when you re-run the KCL auto-gen generate command.

## Schema RollingUpdateStatefulSetStrategy

RollingUpdateStatefulSetStrategy is used to communicate parameter for RollingUpdateStatefulSetStrategyType.

### Attributes

|Name and Description|Type|Default Value|Required|
|--------------------|----|-------------|--------|
|**partition**<br />Partition indicates the ordinal at which the StatefulSet should be partitioned. Default value is 0.|int|Undefined|optional|
<!-- Auto generated by kcl-doc tool, please do not edit. -->