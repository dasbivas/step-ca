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
```
echo "password" | base64 > password.txt
helm install -f values.yaml \
     --set inject.secrets.ca_password=$(cat password.txt) \
     --set inject.secrets.provisioner_password=$(cat password.txt) \
     --set service.targetPort=9000 \
     step-certificates smallstep/step-certificates
```
```
helm install -n platform -f values.yaml \
     --set inject.secrets.ca_password=$(cat password.txt) \
     --set inject.secrets.provisioner_password=$(cat password.txt) \
     --set service.type=NodePort \
     --set service.nodePort=31000  \
     --set service.targetPort=9000 \
     step-certificates smallstep/step-certificates
```
