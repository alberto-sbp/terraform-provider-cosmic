---
layout: "cosmic"
page_title: "Cosmic: cosmic_static_route"
sidebar_current: "docs-cosmic-resource-static-route"
description: |-
  Creates a static route.
---

# cosmic_static_route

Creates a static route for the given private gateway or VPC.

## Example Usage

```hcl
resource "cosmic_static_route" "default" {
  cidr       = "10.0.0.0/16"
  gateway_id = "76f607e3-e8dc-4971-8831-b2a2b0cc4cb4"
}
```

## Argument Reference

The following arguments are supported:

* `cidr` - (Required) The CIDR for the static route. Changing this forces
    a new resource to be created.

* `nexthop` - (Required) The IP address of the nexthop this static route should 
    forward traffic to for the given CIDR. Changing this forces a new resource 
    to be created.

* `vpc_id` - (Required) The VPC ID in which to create this Private gateway. Changing
    this forces a new resource to be created.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the static route.

## Import (EXPERIMENTAL)

Static routes can be imported; use `<STATIC ROUTE ID>` as the import ID. For
example:

```shell
terraform import cosmic_static_route.default e42a24d2-46cb-4b18-9d41-382582fad309
```
