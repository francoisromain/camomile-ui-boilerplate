# Camomile UI boilerplate simple

> A simple boilerplate for [Camomile-ui](https://github.com/francoisromain/camomile-ui).

A similar (more advanced) project using npm and webpack is available here: [Camomile UI boilerplate](https://github.com/francoisromain/camomile-ui-boilerplate).

---

## Directory structure

```bash
.
+-- libs
|   +-- camomile-client.min.js
|   +-- vue.min.js
|   +-- vuex.min.js
|   +-- camomile-ui.min.js
+-- index.html
+-- README.md
```

### /libs

The project dependencies:

* [camomile-client-javascript](https://github.com/camomile-project/camomile-client-javascript)
* [Vue.js](https://vuejs.org/)
* [Vuex](https://vuex.vuejs.org/)
* [Camomile UI](https://www.npmjs.com/package/@camomile/camomile-ui)

### index.html

**The only file that needs to be edited to build an application.**

---

## Getting started (local dev environment)

1.  Clone this repo on your computer.

2.  Open `index.html` from a local server (For example, with node [http-server](https://www.npmjs.com/package/http-server)).

3.  Camonile UI is a front end application only and requires a connection to a [Camomile API server](https://github.com/camomile-project/camomile-server). Clone the Camomile API server in a directory next to this one. Create an additional `camomile-data` directory, resulting in the following structure:

```txt
.
+-- camomile-ui-boilerplate-simple
+-- camomile-server
+-- camomile-data
    +-- mongodb
        +-- files
    +-- camomile
        +-- logs
    +-- media
    +-- upload
```

Set env variables and start the API server:

```bash
export CMML_DB=../camomile-data/mongodb/files && export CMML_LOGS=../camomile-data/camomile/logs && export CMML_MEDIA=../camomile-data/media && export CMML_UPLOAD=../camomile-data/upload && export CMML_PORT=3000 && export CMML_PASSWORD=roO7p4s5wOrD && docker-compose -f ../camomile-server/docker-compose.dev.yml up --build -d
```

4.  Start building your Camomile interface inside the `index.html` file.
