# 🚀 My Awesome Dev Setup 🚀

This repository houses a collection of Docker-based development environments and configurations for various services. It's designed to provide quick and isolated setups for different tech stacks.

## 📁 Directory Structure Overview

Here's a breakdown of what you'll find in this repository:

  * **`./cms`**: Content Management Systems 🌐

      * **`./cms/php`**: PHP-based CMS solutions.
          * **`./cms/php/wordpress`**: 📝 WordPress development environment.
              * `docker-compose.yml`: Docker Compose file to spin up WordPress with a database.
              * `nginx_conf/default.conf`: NGINX configuration for the WordPress setup.

  * **`./databases`**: Database Solutions 🗄️

      * **`./databases/nosql`**: NoSQL database setups.
          * **`./databases/nosql/mongodb`**: 🍃 MongoDB environment.
              * `docker-compose.yml`: Docker Compose for MongoDB (potentially with Mongo Express).
      * **`./databases/sql`**: SQL database setups.
          * **`./databases/sql/postgresql`**: 🐘 PostgreSQL environment.
              * **`./databases/sql/postgresql/psql_pgadmin`**: PostgreSQL with pgAdmin for easy management.
                  * `docker-compose.yml`: Docker Compose for PostgreSQL and pgAdmin.

  * **`./proxy`**: Proxy Services 🛡️

      * **`./proxy/squid`**: 🦑 Squid Proxy server configuration.
          * `cert/`: Directory for SSL certificates.
              * `CA.der`, `CA.pem`, `private.pem`: Certificate files for Squid SSL interception (if configured).
          * `docker-compose.yml`: Docker Compose file for the Squid proxy.

## ⚡ Getting Started

Navigate into the specific service directory you want to run (e.g., `./cms/php/wordpress` or `./databases/nosql/mongodb`) and execute:

```bash
docker-compose up -d
```

This will spin up the necessary containers. Refer to the `docker-compose.yml` file within each directory for specific port mappings and configurations.

## 🤝 Contributing

Feel free to expand on this structure, add more services, or improve existing configurations\! Pull requests are welcome.

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT). (You can choose your preferred license here).