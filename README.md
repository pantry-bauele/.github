
# Pantry

A food-tracking solution built with MongoDB, Express, React, and Node.js.

<img  src="https://bauele.com/pantry-screenshot.png" width="250" />

## Installation

### pantry-backend
First, clone and build the back-end server.
```bash
$ git clone https://github.com/pantry-bauele/pantry-backend.git
$ cd pantry-backend

$ git checkout dev
$ git submodule init
$ git submodule update

$ npm install
$ npm run build
```
example.env provides a listing of all the configuration variables that are expected to be set for the program to function as intended. This should be copied into a .env and the values should be modified to reflect the particular machine's setup.

```bash
$ cp example.env .env
```

**Required**
- DB_* : Expected to be actual MongoDB credentials, otherwise all database operations will fail.
- FIREBASE_SERVICE_KEY_PATH : Expected to be an actual credential issued by Firebase, otherwise server will terminate at launch.

**Optional**
- SERVER_PORT : Program will default to port 3001.
- SERVER_CORS_ORIGIN : Program will default to an insecure * origin.
- SERVER_SSL_* : Program will launch on HTTP instead of HTTPS if certificates are not found.

Once project variables are set, launch the server using
```bash
$ node tsc-built/src/index
```
### pantry-react
Next, clone front-end client in its own directory and start it.
```bash
$ git clone https://github.com/pantry-bauele/pantry-react.git
$ cd pantry-react

$ git checkout dev
$ git submodule init
$ git submodule update

$ npm install
$ npm run sass
```
example.env provides a listing of all the configuration variables that are expected to be set for the program to function as intended. This should be copied into a .env and the values should be modified to reflect the particular machine's setup.

```bash
$ cp example.env .env
```
**Required**
- REACT_APP_SERVER_ADDRESS : Expected to be the server address pantry_backend is running on, otherwise all server requests will fail.
- REACT_APP_SERVER_PORT : Expected to be the port of the server address pantry_backend is running on, otherwise all server requests will fail.

Finally, start the front-end client.
```bash
$ npm run start
```

Everything should now be ready to go!
