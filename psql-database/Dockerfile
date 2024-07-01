# Use the official PostgreSQL image from the Docker Hub
FROM postgres:latest

# Environment variables for PostgreSQL
ENV POSTGRES_DB=employees
ENV POSTGRES_USER=test
ENV POSTGRES_PASSWORD=1234

# Copy initialization SQL script to the Docker image
COPY init-db.sql /docker-entrypoint-initdb.d/

# Copy custom PostgreSQL configuration file
COPY postgresql.conf /etc/postgresql/postgresql.conf

# Expose the PostgreSQL port
EXPOSE 5432

# Ensure PostgreSQL uses the custom configuration
CMD ["postgres", "-c", "config_file=/etc/postgresql/postgresql.conf"]
