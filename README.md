# My docker-compose templates (testing/nonprod)

This repository houses a collection of Docker-based development environments and configurations for various services. It's designed to provide quick and isolated setups for different tech stacks.

## Directory Structure Overview

Here's a breakdown of what you'll find in this repository:

  * **`./cms`**: Content Management Systems

      * **`./cms/php`**: PHP-based CMS solutions.
          * **`./cms/php/wordpress`**: WordPress development environment.
              * `docker-compose.yml`: Docker Compose file to spin up WordPress with a database.
              * `nginx_conf/default.conf`: NGINX configuration for the WordPress setup.

  * **`./databases`**: Database Solutions

      * **`./databases/nosql`**: NoSQL database setups.
          * **`./databases/nosql/mongodb`**: MongoDB environment.
              * `docker-compose.yml`: Docker Compose for MongoDB (potentially with Mongo Express).
      * **`./databases/sql`**: SQL database setups.
          * **`./databases/sql/postgresql`**: 🐘 PostgreSQL environment.
              * **`./databases/sql/postgresql/psql_pgadmin`**: PostgreSQL with pgAdmin for easy management.
                  * `docker-compose.yml`: Docker Compose for PostgreSQL and pgAdmin.

  * **`./message_brokers`**: Message Brokers

      * **`./message_brokers/kafka`**: Apache Kafka with Zookeeper.
          * `docker-compose.yml`: Docker Compose for Kafka and Zookeeper.
          * `.env`: Environment variables for Kafka and Zookeeper ports.
      * **`./message_brokers/rabbitmq`**: RabbitMQ message broker.
          * `docker-compose.yml`: Docker Compose for RabbitMQ with management UI.

  * **`./proxy`**: Proxy Services

      * **`./proxy/squid`**: Squid Proxy server configuration.
          * `docker-compose.yml`: Docker Compose file for the Squid proxy.

  * **`./security`**: Security Tools

      * **`./security/hashicorp_vault`**: HashiCorp Vault secrets management.
          * `docker-compose.yml`: Docker Compose for HashiCorp Vault in dev mode.

## Getting Started

Navigate into the specific service directory you want to run (e.g., `./cms/php/wordpress` or `./databases/nosql/mongodb`) and execute:

```bash
docker-compose up -d
```

This will spin up the necessary containers. Refer to the `docker-compose.yml` file within each directory for specific port mappings and configurations.

## Contributing

Feel free to expand on this structure, add more services, or improve existing configurations! Pull requests are welcome.