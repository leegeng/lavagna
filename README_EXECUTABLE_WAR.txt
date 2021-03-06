A second war named lavagna-jetty-console.war will be built. Inside there is an embedded jetty.

You must provide the following properties:

- datasource.driver=org.hsqldb.jdbcDriver | com.mysql.jdbc.Driver | org.postgresql.Driver
- datasource.dialect=HSQLDB | MYSQL | PGSQL
- datasource.url= for example: jdbc:hsqldb:mem:lavagna | jdbc:mysql://localhost:3306/lavagna | jdbc:postgresql://localhost:5432/lavagna
- datasource.username=<username>
- datasource.password=<pwd> 
- spring.profile.active= dev | prod

For example:

>java -Ddatasource.driver=org.hsqldb.jdbcDriver -Ddatasource.dialect=HSQLDB -Ddatasource.url=jdbc:hsqldb:mem:lavagna -Ddatasource.username=sa -Ddatasource.password= -Dspring.profile.active=dev -jar lavagna-jetty-console.war --headless


You can set port and others options too, see: http://simplericity.com/2009/11/10/1257880778509.html

Options:
 --sslProxied        - Running behind an SSL proxy
 --port n            - Create an HTTP listener on port n (default 8080)
 --bindAddress addr  - Accept connections only on address addr (default: accept on any address)
 --forwarded         - Set reverse proxy handling using X-Forwarded-For headers
 --contextPath /path - Set context path (default: /)
 --headless          - Don't open graphical console, even if available
 --help              - Print this help message
 --tmpDir /path      - Temporary directory, default is /tmp
