# Nexus-Helm

1. Create working directory

`mkdir -p devops-tools-install/nexus-np`

`cd devops-tools-install/nexus-np`

2. Create Namespace

`kubectl create ns nexus`

3. Create rolebinding.yaml

4. Create Role Binding

`kubectl apply -f rolebinding.yaml -n nexus`

5. Create value.yaml

6. Run Helm Chart

`helm repo add sonatype https://sonatype.github.io/helm3-charts/`

`helm install nexus sonatype/nexus-repository-manager -f values.yaml -n nexus`

7. Verifications

`kubectl get pod -n nexus`

`kubectl get svc -n nexus`

`kubectl get pvc -n nexus`

`kubectl get serviceaccount -n nexus`

`kubectl get role -n nexus`

`kubectl get rolebinding -n nexus`

8. Create httpproxy.yaml

9. Create HTTPProxy

`kubectl apply -f httpproxy.yaml -n nexus`

`kubectl get httpproxy -n nexus`

`kubectl describe httpproxy nexus-web -n nexus`

# Global Settings
1. Change Default admin password to bct1234

2. Disable anonymous access

3. Create LDAP 
