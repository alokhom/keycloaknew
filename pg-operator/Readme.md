helm repo add percona https://percona.github.io/percona-helm-charts/
helm repo update

helm install pg-operator ./pg-operator-1.4.0.tgz -f values.yaml -n keycloak

or 

helm install pg-operator -f values.yaml -n keycloak