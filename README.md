# ansible-supported-system
* * *

## Description
This role sets the boolean fact _supported_system_ based on a given set of distributions/versions.

It is primarily intended to be included as a role dependency inside a role so unsupported systems won't run the main role.

## Variables

Optional:
- _supported_systems_: dict in the form of {'distribution': '[list of versions]'}.

## Example
_role_/meta/main.yml:
```
---
dependencies:
  - role: supported-system
    supported_systems:
      Ubuntu: [12,14,16]
      Debian: [8]
```
