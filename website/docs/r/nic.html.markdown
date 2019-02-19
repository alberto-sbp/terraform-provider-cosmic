---
layout: "cosmic"
page_title: "Cosmic: cosmic_nic"
sidebar_current: "docs-cosmic-resource-nic"
description: |-
  Creates an additional NIC on an instance in the specified network.
---

# cosmic_nic

Creates an additional NIC on an instance in the specified network.

## Example Usage

Basic usage:

```hcl
resource "cosmic_nic" "test" {
  network_id         = "6eb22f91-7454-4107-89f4-36afcdf33021"
  ip_address         = "192.168.1.1"
  virtual_machine_id = "f8141e2f-4e7e-4c63-9362-986c908b7ea7"
}
```

## Argument Reference

The following arguments are supported:

* `network_id` - (Required) The ID of the network to plug the NIC into. Changing
    this forces a new resource to be created.

* `ip_address` - (Optional) The IP address to assign to the NIC. Changing this
    forces a new resource to be created.

* `virtual_machine_id` - (Required) The ID of the virtual machine to which to
    attach the NIC. Changing this forces a new resource to be created.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the NIC.
* `ip_address` - The assigned IP address.

## Import (EXPERIMENTAL)

NICs can be imported; use `<NIC ID>` as the import ID. For
example:

```shell
terraform import cosmic_nic.default e42a24d2-46cb-4b18-9d41-382582fad309
```
