NBDE and IPI bootstrap internals
=================================

As part of my work on creating an openshift NBDE field guide, I've encountered some interesting observations I'd like to share.

We want to create a field implementation guide for NBDE. That guide will become part of openshift official documentation and include advanced topics like TANG deployment considerations and how to do re-keying operation on OCP. Since it's being officially added, we want to complete CI for everything that we do and in order to do that, we first need to get a properly working NBDE environment.

[NBDE enablement is documented as part of OCP](https://github.com/openshift/openshift-docs/blob/enterprise-4.7/modules/installation-special-config-encrypt-disk-tang.adoc) and [we even have support for that](https://github.com/karmab/kcli-openshift4-baremetal/blob/master/07_nbde.sh) in our development environment kcli plan and that is even [properly updated](https://github.com/karmab/kcli-openshift4-baremetal/blob/master/99-openshift-tang-encryption-clevis.sample.yaml) to the 4.7 method described above.
