  - **What is Clojars ( https://clojars.org/ ) for?**  
  It is community repository for open source Clojure libraries.
  
  - **What is Leiningen ( https://leiningen.org/ )?**  
   Leiningen is the Clojure counterpart of Maven, a popular Java build tool. It uses a Maven-compatible dependency management system, and therefore it has access to large and well-maintained repositories of Java libraries. In addition, Clojure libraries are commonly found in the Clojars repository. This repository is enabled by default in Leiningen.
   
  - **What is Luminus ( http://www.luminusweb.net/ )?**  
  Luminus is a Clojure micro-framework based on a set of lightweight libraries.
  
  - **What is H2 (DBMS) ( http://www.h2database.com/ )?**  
  H2 is a relational database management system written in Java. It can be embedded in Java applications or run in the client-server mode.
  
  - **How to run the new Luminus +H2 project on Linux (e.g. Ubuntu)?**  
1. Place the following code into: `/home/__USER__/.lein/profiles.clj` to follow the same lein-template version:
  `{:user
 {:plugins [[luminus/lein-template "2.9.10.74"]]}}`
2. Run `lein new luminus guestbook +h2` to create a new application by specifying luminus as the template name and guestbook as the project name, and add the +h2 parameter to indicate that we want to have an instance of the H2 embedded database initialized for us.  
3. Run `lein run -p 8000` to start the application on port 8000. When you run the application, it may take a little while because Leiningen first has to retrieve all of its dependencies. Once downloaded, the dependencies are cached locally in the `~/.m2/repository` folder and will be available on subsequent runs.
4. Open a web browser and check for `http://localhost:8000/`

  - **How to create migration files (_datetime_-guestbook.up.sql & _datetime_-guestbook.down.sql) by using `lein`?**  
  `lein migratus create guestbook`
  
  - **How to run migrations by using `lein`?**  
  `lein run migrate`
  
  