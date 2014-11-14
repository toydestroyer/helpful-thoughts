Allow connection from `[remote_ip]` in `/etc/postgresql/9.3/main/pg_hba.conf`

    host    all             all             [remote_ip]/32        md5

Set `listen_addresses` in `/etc/postgresql/9.3/main/postgresql.conf`

    listen_addresses = '[current_ip]'

And reload PostgreSQL

    $ sudo service postgresql reload

Add `ufw` rule to port `5432`:

    $ sudo ufw allow from [remote_ip] to any port 5432

