SDK to connect to the UMMobile API

# Getting Started
This package was made for the UMMobile app.

## Initialization
To initialize a new instance a token is needed.
```dart
UMMobileAPI api = UMMobileAPI(token: 'YOUR_TOKEN');
```

### Auth
To get a token you can use the static function `UMMobileAPI.auth()` that returns the API section for the authentication.
```dart
// Get token
Token token = await UMMobileAPI
  .auth()
  .getToken(username: 1234567, password: 'YOUR_PASSWORD');

// Initialize using the access token
UMMobileAPI api = UMMobileAPI(token: token.accessToken);
```

# Sections
The `UMMobileAPI` contains an attribute for each API section.

- `user`: contains the functions to get the user information.