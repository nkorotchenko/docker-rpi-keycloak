KeyCloak 11.0.0 for raspberry pi 4.

Build image

`docker build -t keycloak .`

Run image

`docker run -d --restart=unless-stopped --name=keycloak -p 8000:8080 -e KEYCLOAK_USER=admin -e KEYCLOAK_PASSWORD=password -e PROXY_ADDRESS_FORWARDING=true -v /data:/opt/jboss/keycloak/standalone/data keycloak`
