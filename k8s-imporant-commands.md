eyJhbGciOiJSUzI1NiIsImtpZCI6IktWVS16cndjTVNKQVBJYWlMVEtobmppTEM3YUZCT3VxQ2F2NzhXNXNvbzgifQ.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJla3MtYWRtaW4tdG9rZW4tOGg2ajkiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC5uYW1lIjoiZWtzLWFkbWluIiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQudWlkIjoiZTY2MDRlNzktMTU4ZC00MjFjLTg1Y2EtNDZmZDU1MWI2Y2EyIiwic3ViIjoic3lzdGVtOnNlcnZpY2VhY2NvdW50Omt1YmUtc3lzdGVtOmVrcy1hZG1pbiJ9.qn7wY5YX2RgNtNrQIKqVw82QOUwFoBQZvvnFCubq1fnmnIsQ-x3jb4_VGGFd8q_cm8J0PeVw_gJ947-VipgkKrcugfjdbbXmItzRtA3q93J2ANRVm-P-eTy7kzR08WahLCt-EqI0v5MLdvnfzphGnT2gcb9PU4TSUqjU8brgFY_rd2vGO7yR1n0wHOxdWcgLPer2Tnme6VYK02KEs43iyMgxsBYPLVKLw7BgwzLNWYvfysctnomRNdXSdlQfuyjQe4i9hUTBXSnv5XBCXsdYMRURj7_7mOF6ZAuRZm9eCyhHe8654tVhIAXYE292mUQZGiC4xHnpVaW4yFHLLBLRag

pass: PYXQ2HbX277GJ0V7opxrW7ur8qDIEAJX


thetechexpert.xyz

kops-state-neeraj



aws s3 cp s3://kops-state-neeraj/thetechexpert.xyz/pki/private/ca/$KEY.key ca.key




aws s3 cp s3://$BUCKET/$CLUSTER/pki/private/ca/$KEY.key ca.key
aws s3 cp s3://$BUCKET/$CLUSTER/pki/issued/ca/$CERT.crt ca.crt


https://github.com/kubernetes-retired



a1424b0492d4d4964a3b85b2fe13d348-1210178101.us-east-1.elb.amazonaws.com


ns-22.awsdns-02.com.
ns-2028.awsdns-61.co.uk.
ns-1169.awsdns-18.org.
ns-882.awsdns-46.net.



HPA: test  
kubectl run -it --rm load-generator --image=busybox /bin/sh
  
while true; do wget -q -O- http://hpa-example.default.svc.cluster.local:31001



sudo openssl x509 -req -in neeraj-csr.pem -CA /var/lib/localkube/certs/ca.crt -CAkey /var/lib/localkube/certs/ca.key -CAcreateserial -out neeraj.crt -days 10000




./root/.minikube/ca.key
./var/lib/minikube/certs/ca.key
./var/lib/minikube/certs/etcd/ca.key





opessl genrsa -out neeraj.pem 2048
vi /etc/ssl/openssl.cnf
openssl req -new -key neeraj.pem -out neeraj-csr.pem -subj "/CN=neeraj/O=myteam/"
sudo openssl x509 -req -in neeraj-csr.pem -CA /var/lib/localkube/certs/ca.crt -CAkey /var/lib/localkube/certs/ca.key -CAcreateserial -out neeraj.crt -days 10000


demo app Chart

## Download dependencies
```
helm dependency update
```

## Install Chart
```
helm install .
```

## Upgrade Chart
```
helm upgrade --set image.tag=v0.0.2,mariadb.db.password=$DB_APP_PASS RELEASE .	




aws s3 cp s3://$BUCKET/$CLUSTER/pki/private/ca/$KEY.key ca.key
aws s3 cp s3://$BUCKET/$CLUSTER/pki/issued/ca/$CERT.crt ca.crt


aws s3 cp s3://kops-state-neeraj/thetechexpert.xyz/pki/private/ca/6830439744076675823832375022.key /var/lib/kops/certs/ca.key
aws s3 cp s3://kops-state-neeraj/thetechexpert.xyz/pki/issued/ca/6830439744076675823832375022.crt /var/lib/kops/certs/ca.crt

Download the kops-generated CA certificate and signing key from S3:
s3://<BUCKET_NAME>/<CLUSTER_NAME>/pki/private/ca/*.key
s3://<BUCKET_NAME>/<CLUSTER_NAME>/pki/issued/ca/*.crt
Generate a client key: openssl genrsa -out neeraj-key.pem 2048
Generate a CSR:

openssl req -new -key neerajs-key.pem -out neerajs-csr.pem -subj "/CN=neeraj/O=myteam" 
Generate a client certificate:

openssl x509 -req -in neerajs-csr.pem -CA /var/lib/kops/certs/ca.crt -CAkey /var/lib/kops/certs/ca.key -CAcreateserial -out neerajs-crt.pem -days 10000
Base64-encode the client key, client certificate, and CA certificate, and populate those values in a config.yml, e.g. this
Distribute the populated config.yml to your developers.


client-certificate: /var/lib/kops/certs/newUsercerts/neerajs-crt.pem
client-key: /var/lib/kops/certs/newUsercerts/neeraj-key.pem



openssl x509 -req -in neerajs-csr.pem -CA /var/lib/kops/certs/ca.crt -CAkey /var/lib/kops/certs/ca.key -CAcreateserial -out neerajns-crt.pem -days 10000


openssl x509 -req -in neerajs-csr.pem -CA /var/lib/kops/certs/ca.crt -CAkey /var/lib/kops/certs/ca.key -CAcreateserial -out neerajns.crt -days 10000


kubectl config set-credentials neeraj --client-certificate=/var/lib/kops/certs/newUsercerts/neerajns.crt --client-key=/var/lib/kops/certs/newUsercerts/neeraj-key.pem
kubectl config set-context neeraj --cluster=thetechexpert.xyz --user neeraj


kubectl config get-contexts

kubectl config use-context neeraj

etcd backups:::

./etcd-manager-ctl -backup-store s3://kops-state-neeraj/thetechexpert.xyz/backups/etcd/main/ list-backups


kubectl run --namespace default myredis1-client --rm --tty -i --restart='Never' --env REDIS_PASSWORD=$REDIS_PASSWORD --image docker.io/bitnami/redis:latest -- bash



kops create cluster --name=thetechexpert.xyz --state=s3://kops-state-neeraj --zones=us-east-1a --node-count=2 --node-size=t2.micro --master-size=t2.micro --dns-zone=thetechexpert.xyz
kops update cluster thetechexpert.xyz --state=s3://kops-state-neeraj --yes
kops edit cluster thetechexpert.xyz --state=s3://kops-state-neeraj 
kops delete cluster thetechexpert.xyz --state=s3://kops-state-neeraj --yes

kops validate cluster thetechexpert.xyz --state=s3://kops-state-neeraj
