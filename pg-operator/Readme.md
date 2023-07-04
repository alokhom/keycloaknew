
helm install pg-operator ./pg-operator-1.4.0.tgz -f values.yaml -n keycloak

helm install pg-db ./pg-db-1.4.0.tgz -f values.yaml -n keycloak