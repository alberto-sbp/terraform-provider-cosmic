# CHANGELOG

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/) and this project adheres to [Semantic Versioning](http://semver.org/).

## Unreleased

- Add option to configure provider using `COSMIC_CONFIG` and `COSMIC_PROFILE` environment variables
- Changing `cosmic_network`'s `ip_exclusion_list` option no longer recreates the resource
- Changing `cosmic_vpc`'s `vpc_offering` option no longer recreates the resource

## 0.1.0 (2019-01-27)

First versioned release.

Recent additions include:

- Add `config` and `profile` options to configure cosmic provider using a cloudmonkey config
- Add `optimise_for` option for `cosmic_instance`
- Add `protocol` option for `cosmic_loadbalancer_rule`
- Add `terraform import ...` support to cosmic resources to import existing infrastructure
