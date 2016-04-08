# Doppio API

## Requirements

- node and npm

## Usage

1. Clone the repo: `git clone https://github.com/coosamatt/doppio_api.git`
2. Install dependencies: `npm install`
3. Change SECRET in `config.js`
4. Add your own MongoDB database to `config.js`
5. Start the server: `node server.js`
6. Create sample user by visiting: `http://localhost/setup`

Once everything is set up, we can begin to use our app by creating and verifying tokens.

### Getting a Token

Send a `POST` request to `http://localhost/api/authenticate` with test user parameters as `x-www-form-urlencoded`. 

```
  {
    name: 'Nick Cerminara',
    password: 'password'
  }
```

### Verifying a Token and Listing Users

Send a `GET` request to `http://localhost/api/users` with a header parameter of `x-access-token` and the token.

You can also send the token as a URL parameter: `http://localhost/api/users?token=YOUR_TOKEN_HERE`

Or you can send the token as a POST parameter of `token`.
