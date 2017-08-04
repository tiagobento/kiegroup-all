After cloning...
---

`git submodule init;`

`git submodule foreach git checkout master;`

`git submodule foreach git pull origin master;`

`mvn clean install --fail-at-end;`

**NOTE:** Setting `MAVEN_OPTS="-Xmx8192m"` may be necessary.


Choosing what to build
---

`mvn clean install -pl "uberfire"` will build only uberfire

`mvn clean install -pl "\!uberfire"` will build everything except uberfire
