# step-ca
Own Certificate Authority Follow the steps
https://artifacthub.io/packages/helm/smallstep/step-certificates

# Install Step CA
```
1.https://smallstep.com/docs/step-cli/installation/#linux-packages-amd64
2.step ca init --helm > values.yaml
Provisoner Name: acme/development
DNS: serviceName/ Own DNS
TYPE:ACME Note: Need to chane in Values.yaml
Password: with special words eg.abc@123

```
