`# Multi-Tier Architecture: Two-Tier Deployment

## The Web/Application Tier

The web or application tier is represented by the Nextcloud `app` container, which is the main part that users interact with. It provides the web interface, receives HTTP requests through port 8080, and manages tasks such as file uploads, user logins, and file sharing. When information needs to be saved, the application communicates with the database tier.

## The Database Tier

The database tier is handled by the `database` container, which runs MariaDB. It stores important persistent information such as user accounts, login details, file metadata, and sharing permissions. The database is not directly accessible from the public internet and only accepts requests from the application tier.

## Why Separate Them?

Keeping the web application and database in separate containers makes the system easier to manage because each component can be updated, restarted, or scaled independently. For example, updating the Nextcloud application does not require stopping the database. This setup also improves security because the database is protected from direct internet access and can only be reached through the internal Docker network used by the application.

