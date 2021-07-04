# Automatic Certificate Rotation

## CRD

Here we need a `Custom Resource Definition`. So we Add `cert-manager` in kubernetes from [here](https://cert-manager.io/docs/installation/kubernetes/)

We got three custom resource Definitions

1. Issuer: used to issue certificates (bound single namespace)
2. ClusterIssuer: work is same as Issuer ( Not BOunded to single namespace)
3. Certificate: Desire State of certificate and request certificate from issuer when expire.

## How its works:

1.

### Command To Check Progress:

1. Status of CertificateRequest

```sh
kubectl describe CertificateRequest -A
```

2. Get All Issuers

```
kubectl get issuers -A
```

3. Get all Certificate

```sh
kubectl get certificate -A
```

4. Get All Challenges

```sh
kubectl get challenge -A
```
