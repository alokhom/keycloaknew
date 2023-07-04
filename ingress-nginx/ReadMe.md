openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout tls.key -out tls.crt -subj "/CN=mvp.com/O=mvp.com" -addext "subjectAltName = DNS:mvp.com"

kubectl -n keycloak create secret tls keycloak-tls-secret --key ingresstls.key --cert ingresstls.crt

helm install ingress-nginx ingress-nginx/ingress-nginx -f values.yaml -n ingress-nginx --create-namespace