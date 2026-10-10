<p align="center">
  <img src="assets/camille.png" alt="Camille, the mascot of Liko" width="240">
</p>

<h1 align="center">prometheus-operator.liko</h1>

**This repository contains the Prometheus Operator module for the Liko data language. This module is officially maintained by the Liko team.**

It contains the complete set of Prometheus Operator schema definitions from the official [Prometheus Operator repository](https://github.com/prometheus-operator/prometheus-operator/releases).

---

## Installation

Initialize a local module with `liko init`, then add `prometheus-operator.liko` as a dependency.

```bash
liko init
```
```bash
liko add prometheus-operator
```

```bash
liko install
```

## Usage

The module can now be used from any directory within the current module.

```liko
#Po: import "prometheus-operator/v1"

$: #Po.Alertmanager & {
    spec: {
       alertmanagerConfiguration: {
           name: "my-am"
       } 
    }
    
}
```
