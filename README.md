`init-letsencrypt.sh` script will get and renewal of a Let’s
Encrypt certificate for your domain. Docker Compose will then start 
Artifactory with nginx as a reverse proxy using the Lets Encrypt certs.

1. Modify configuration:
- Add domains and email addresses to init-letsencrypt.sh
- Replace all occurrences of artifactory.chadmetcalf.com with your domain in data/nginx/app.conf

2. Run the init script:

        ./init-letsencrypt.sh

3. Run the server:

        docker-compose up

Acknowledgements:

Thanks to https://github.com/wmnnd/nginx-certbot for the starting point.
