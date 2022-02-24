# CiaB Build Action

This action will build a set of kolla containers, using the Chameleon build customizations.


Example syntax for use in other workflows:

```yml
---
name: build_stuff
on: [push]
env:
  DOCKER_REGISTRY: docker.chameleoncloud.org
  KOLLA_NAMESPACE: kolla-dev
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: build-action
        uses: msherman64/kolla-containers@master
```
