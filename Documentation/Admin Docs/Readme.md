This page along with it's subpages contains admin documentation for the selfhosted open-source cloudservice Nextcloud with open-source office tools provided by Collabora using Docker. The documentation consists of two parts. Setup and Management of the server.

At the heart of Techlabs Nextcloud is Docker. We use Docker to deploy 4 containers, each with a specific role.

1. linuxserver/swag
2. linuxserver/nextcloud
3. linuxserver/mariadb
4. collabora/code

The first container is called swag, provided by the [linuxserver.io](https://www.linuxserver.io/) open-source community.

> SWAG - Secure Web Application Gateway sets up an Nginx webserver and reverse proxy with php support and a built-in certbot client that automates free SSL server certificate generation and renewal processes (Let's Encrypt and ZeroSSL). It also contains fail2ban for intrusion prevention.

We use SWAG as described above. It works as our reverse proxy for Nextcloud and Collabora services and it automates Let's Encrypt SSL certificate generation for HTTPS. Additionally we use fail2ban for  added security. If someone tries to login with wrong credentials too many times they get IP banned for a specific amount of time.

Next we have the Nextcloud container which contains the Nextcloud files and an Nginx webserver. It uses the Mariadb container as it's database. Nextcloud doesn't ship Office tools like Word or Excel by default. This is why we have the collabora/code container, it provides the tools for creating advanced word documents, spreadsheets, presentations and diagrams.

\_____________________\_

> Mikä tämä on?
>
> Mitä tällä tehdään?
>
> Miten sitä käytetään?
>
> Mitä on siitä hyötyä?
>
> Mitä tarvitset asennukseen ja hallintointiin?
>
> 1. Asennus
>
> \-
>
> \-
>
> \-
>
> \-
>
> 1. Hallinnointi
>
> \-
>
> \-
>
> \-
>
> \-
>
> Käyttöön liittyviä huomioita
>
> Yhteenveto
>
> Tekijä