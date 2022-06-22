# downward_api_projection

Source: [base/pkg/kusion_kubernetes/api/core/v1/downward_api_projection.k](https://github.com/KusionStack/konfig/tree/main//base/pkg/kusion_kubernetes/api/core/v1/downward_api_projection.k)

This is the downward\_api\_projection module in kusion\_kubernetes.api.core.v1 package.<br />This file was generated by the KCL auto-gen tool. DO NOT EDIT.<br />Editing this file might prove futile when you re-run the KCL auto-gen generate command.

## Schema DownwardAPIProjection

Represents downward API info for projecting into a projected volume. Note that this is identical to a downwardAPI volume source without the default mode.

### Attributes

|Name and Description|Type|Default Value|Required|
|--------------------|----|-------------|--------|
|**items**<br />Items is a list of DownwardAPIVolume file|[[v1.DownwardAPIVolumeFile](doc_downward_api_volume_file.md#schema-downwardapivolumefile)]|Undefined|optional|
<!-- Auto generated by kcl-doc tool, please do not edit. -->