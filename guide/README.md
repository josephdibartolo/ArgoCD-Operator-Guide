# Install Guide for ArgoCD (v0.0.8)

## Sourcing the Operator

ArgoCD's Operator can be installed either through the Openshift *OperatorHub*, or by manually applying the resource to the cluster. We outline both steps below.

### OperatorHub

Go to the OperatorHub and search for ArgoCD. You will see two versions come up, one for a Helm install and one without Helm. We will use the one **without** Helm, simply entitled `ArgoCD`.

You will need to install the ArgoCD Operator to a particular namespace; one recommended strategy is to create a project/namespace entitled `argocd` and use this for all ArgoCD-related resources. Click `Install` and configure ArgoCD to whatever namespace you want to use.

The operator will spin-up in the selected project/namespace.

### Manually

Please refer to [ArgoCD's documentation](https://argocd-operator.readthedocs.io/en/latest/install/openshift/) for details how to do a manual install of the operator. (I do **not** recommend this method for scenarios where it is possible to use the OperatorHub to install the Operator.)

## Instantiating ArgoCD

There exist and handful of pre-defined configurations for a handful of use-cases, such as High Availability. The YAML for these templates can be found in the [examples section](https://github.com/argoproj-labs/argocd-operator/tree/master/examples) of the [ArgoCD Operator repository](https://github.com/argoproj-labs/argocd-operator) on GitHub.

There are many options for configuring a particular ArgoCD instance. The documentation for all the possible configuration options for the `ArgoCD` custom-resource can be found in the [reference documentation here](https://argocd-operator.readthedocs.io/en/latest/reference/argocd/).

There are a few key features we will highlight in this guide below.
