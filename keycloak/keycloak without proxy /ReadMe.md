openssl req -subj '/CN=keycloak.mvp.com/O=Test Keycloak./C=US' -newkey rsa:2048 -nodes -keyout key.pem -x509 -days 365 -out certificate.pem

kubectl -n keycloak create secret tls example-tls-secret --cert certificate.pem --key key.pem