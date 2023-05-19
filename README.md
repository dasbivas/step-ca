# step-ca
Own Certificate Authority 
**Helm Chart:**
```
https://artifacthub.io/packages/helm/smallstep/step-certificates
```
**Package Installation:**
```
https://smallstep.com/docs/step-cli/installation/#linux-packages-amd64
```
# Install Step CA
```
step ca init --helm > values.yaml
Provisoner Name: acme/development
DNS: serviceName/ Own DNS
TYPE:ACME Note: Need to chane in Values.yaml
Password: with special words eg.abc@123

```
