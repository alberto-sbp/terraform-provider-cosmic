---
layout: "cosmic"
page_title: "Cosmic: cosmic_private_gateway"
sidebar_current: "docs-cosmic-resource-private-gateway"
description: |-
  Creates a private gateway.
---

# cosmic_private_gateway

Creates a private gateway for the given VPC.

*NOTE: private gateway can only be created using a ROOT account!*

## Example Usage

```hcl
resource "cosmic_private_gateway" "default" {
  gateway    = "10.0.0.1"
  ip_address = "10.0.0.2"
  netmask    = "255.255.255.252"
  vlan       = "200"
  vpc_id     = "76f6e8dc-07e3-4971-b2a2-8831b0cc4cb4"
}
```

## Argument Reference

The following arguments are supported:

* `ip_address` - (Required) the IP address of the Private gateway. Changing this forces
    a new resource to be created.

* `network_id` - (Required) The ID of the private gateway network this private
    gateway belongs to.

* `acl_id` - (Required) The ACL ID that should be attached to the private gateway.

* `vpc_id` - (Required) The VPC ID in which to create this Private gateway. Changing
    this forces a new resource to be created.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the private gateway.

## Import (EXPERIMENTAL)

Private gateways can be imported; use `<PRIVATE GATEWAY ID>` as the import ID. For
example:

```shell
terraform import cosmic_private_gateway.default e42a24d2-46cb-4b18-9d41-382582fad309
```
