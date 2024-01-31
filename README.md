#Welcome to my basic server container!
    This is a dockerized apache and mysql server environment.
The repository contains only the necessary configuration and 
Dockerfiles.

##Setting Up the Environment
    ###Step 1: Have the Docker Engine running
        Ensure that Docker is installed on the your machine
        and that the Docker engine is running.
    
    ###Step 2: Import your web files into ./web
        Drop your webfiles into the web directory to serve
        the pages.

        The contents of ./web are copied into the apache
        container's /var/www/html/ path.  Apache's entrypoint is index.* 
        so it is recommended that you have a index.html or index.php in
        ./web
    3. 
    ###Step 3: Seed the database for use
        In order to seed the database for your application, replace the 
        seedfile in ./database/migrations/ with your own seedfile.

        To create a seedfile, connect to the database using mysql, 
        mysqlworkbench, or any other database interface.  According to the
        configuration defined in the docker-compose.yml file, the user will
        be root and there will be no password.  It is recommended that you
        change this to be more secure in production environments.  
        Once you have connected to the database, create your table and export
        the database into the seed file.

    ###Step 4: Launch the application
        In order to launch the application, run a `docker compose up`.

##Is It Working?
    If you run `docker compose up` locally on this blank repository, you should
    see the php version page at http://localhost:80 