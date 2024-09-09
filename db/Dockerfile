# Use the official PostgreSQL image from Docker Hub
FROM postgres:14

# Set environment variables for PostgreSQL
ENV POSTGRES_DB=mydatabase
ENV POSTGRES_USER=myuser
ENV POSTGRES_PASSWORD=mypassword

# Copy custom configuration files if any
COPY ./postgresql.conf /etc/postgresql/postgresql.conf
COPY ./pg_hba.conf /etc/postgresql/pg_hba.conf

# Expose PostgreSQL port
EXPOSE 5432

# Set default command to run PostgreSQL server
CMD ["postgres", "-c", "config_file=/etc/postgresql/postgresql.conf"]
