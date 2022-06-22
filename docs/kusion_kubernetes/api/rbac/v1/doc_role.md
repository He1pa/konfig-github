# role

Source: [base/pkg/kusion_kubernetes/api/rbac/v1/role.k](https://github.com/KusionStack/konfig/tree/main//base/pkg/kusion_kubernetes/api/rbac/v1/role.k)

This is the role module in kusion\_kubernetes.api.rbac.v1 package.<br />This file was generated by the KCL auto-gen tool. DO NOT EDIT.<br />Editing this file might prove futile when you re-run the KCL auto-gen generate command.

## Schema Role

Role is a namespaced, logical grouping of PolicyRules that can be referenced as a unit by a RoleBinding.

### Attributes

|Name and Description|Type|Default Value|Required|
|--------------------|----|-------------|--------|
|**apiVersion**<br />APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md\#resources|"rbac.authorization.k8s.io/v1"|"rbac.authorization.k8s.io/v1"|**required**|
|**kind**<br />Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md\#types-kinds|"Role"|"Role"|**required**|
|**rules**<br />Rules holds all the PolicyRules for this Role|[[v1.PolicyRule](doc_policy_rule.md#schema-policyrule)]|Undefined|optional|
|**metadata**<br />Standard object's metadata.|[apis.ObjectMeta](../../../apimachinery/apis/doc_object_meta.md#schema-objectmeta)|Undefined|optional|
<!-- Auto generated by kcl-doc tool, please do not edit. -->