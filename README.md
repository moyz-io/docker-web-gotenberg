# Docker web Gotenberg

This tool is to manage or create PDF.

The service is named [Gotenberg](https://gotenberg.dev/).

## Set up

First, you must up the tool:

    $ docker-compose up -d

You can link your service with this tools by add network in your docker-compose file :

    ...
    
    networks:
        server_gotenberg:
            external: true

    services:
        your_service:
            ...
            networks:
                ...
                - server_gotenberg


Then, the service is available on `gotenberg:3000`.