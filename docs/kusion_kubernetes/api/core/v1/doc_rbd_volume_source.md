# rbd_volume_source

Source: [base/pkg/kusion_kubernetes/api/core/v1/rbd_volume_source.k](https://github.com/KusionStack/konfig/tree/main//base/pkg/kusion_kubernetes/api/core/v1/rbd_volume_source.k)

This is the rbd\_volume\_source module in kusion\_kubernetes.api.core.v1 package.<br />This file was generated by the KCL auto-gen tool. DO NOT EDIT.<br />Editing this file might prove futile when you re-run the KCL auto-gen generate command.

## Schema RBDVolumeSource

Represents a Rados Block Device mount that lasts the lifetime of a pod. RBD volumes support ownership management and SELinux relabeling.

### Attributes

|Name and Description|Type|Default Value|Required|
|--------------------|----|-------------|--------|
|**fsType**<br />Filesystem type of the volume that you want to mount. Tip: Ensure that the filesystem type is supported by the host operating system. Examples: "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. More info: https://kubernetes.io/docs/concepts/storage/volumes\#rbd|str|Undefined|optional|
|**image**<br />The rados image name. More info: https://examples.k8s.io/volumes/rbd/README.md\#how-to-use-it|str|Undefined|**required**|
|**keyring**<br />Keyring is the path to key ring for RBDUser. Default is /etc/ceph/keyring. More info: https://examples.k8s.io/volumes/rbd/README.md\#how-to-use-it|str|Undefined|optional|
|**monitors**<br />A collection of Ceph monitors. More info: https://examples.k8s.io/volumes/rbd/README.md\#how-to-use-it|[str]|Undefined|**required**|
|**pool**<br />The rados pool name. Default is rbd. More info: https://examples.k8s.io/volumes/rbd/README.md\#how-to-use-it|str|Undefined|optional|
|**readOnly**<br />ReadOnly here will force the ReadOnly setting in VolumeMounts. Defaults to false. More info: https://examples.k8s.io/volumes/rbd/README.md\#how-to-use-it|bool|Undefined|optional|
|**user**<br />The rados user name. Default is admin. More info: https://examples.k8s.io/volumes/rbd/README.md\#how-to-use-it|str|Undefined|optional|
|**secretRef**<br />SecretRef is name of the authentication secret for RBDUser. If provided overrides keyring. Default is nil. More info: https://examples.k8s.io/volumes/rbd/README.md\#how-to-use-it|[LocalObjectReference](doc_local_object_reference.md#schema-localobjectreference)|Undefined|optional|
<!-- Auto generated by kcl-doc tool, please do not edit. -->