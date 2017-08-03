After cloning...
---

`git submodule init;`

`git submodule update --remote;`

`mvn clean install --fail-at-end;`

Sit back and wait :)

Choosing what to build
---

`mvn clean install -pl "uberfire"` will build only uberfire

`mvn clean install -pl "\!uberfire"` will build everything except uberfire
