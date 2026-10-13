---
name: internet2-add-person-to-group
description: Create a new person, create a group, and add the person as a member of that group.
api: openapi/comanage-registry-restapiv1.yml
operations:
- addCoPerson
- addCoGroup
- addCoGroupMember
generated: '2026-10-13'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/comanage-registry-restapiv1.yml ; every operationId checked against the contract
---

# internet2-add-person-to-group

Create a new person, create a group, and add the person as a member of that group.

## Steps

1. 1. Use `addCoPerson` with the person fields in the request body and include the Basic Authorization header.
2. 2. Use `addCoGroup` with the group fields in the request body and include the Basic Authorization header.
3. 3. Use `addCoGroupMember` with the membership fields (person ID and group ID) in the request body and include the Basic Authorization header.

## Rules

- All requests require a Basic Authorization header as defined by the `basicAuth` scheme.
- POST operations (`addCoPerson`, `addCoGroup`, `addCoGroupMember`) are not idempotent; repeat submissions may create duplicate resources.
