After cloning...
---

`git submodule init;`

`git submodule update --remote;`

`git submodule foreach git checkout master;` #just to be sure

`git submodule foreach git pull origin master;` #just to be sure

`mvn clean install --fail-at-end;`

**NOTE:** Setting `MAVEN_OPTS="-Xmx8192m"` may be necessary.

**NOTE2:** Creating an alias for `git submodule foreach` can come in handy. (e.g. `alias gsf='git submodule foreach'`)

**TIP:** Add all your forks: e.g. `gsf "pwd | xargs basename | xargs -I{} git remote add fork git@github.com:github_user/{}.git || echo 'Ignore'"`

**TIP2:** Prevent from accidentaly pushing to origin `gsf git remote set-url --push origin no_push`.


Choosing what to build
---

`mvn clean install -pl "uberfire"` will build only uberfire

`mvn clean install -pl "\!uberfire"` will build everything except uberfire
