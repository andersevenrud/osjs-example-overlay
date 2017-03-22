# Example OS.js overlay

This is an example overlay for OS.js.

This is used to add client and server modules, etc.

**This is intended for the future 2.0.0-89 release. Everything except packges is working.**

## Configuration

If you clone this into your OS.js installation as `overlays/example`, place this in your custom json configuration file:
```json
{
  "server": {
    "overlays": {
      "example": {
        "packages": [
          "overlays/example/packages"
        ],
        "modules": [
          "overlays/example/server"
        ]
      }
    }
  },
  "build": {
    "overlays": {
      "example": {
        "packages": [
          "overlays/example/packages"
        ],
        "templates": [
          "overlays/example/templates"
        ],
        "javascript": [
          "overlays/example/client/javascript/example.js"
        ],
        "locales": [
          "overlays/example/client/locales/example.js"
        ],
        "stylesheets": [
          "overlays/example/client/stylesheets/example.css"
        ]
      }
    }
  }
}
```

This way you can for example define custom modules:

```json
{
  "authenticator": "example",
  "storage": "example",
  "repositories": [
    "default",
    "example"
  ],
  "build": {
    "dist": {
      "template": "example",
      "splash": "example",
      "login": "example"
    }
  }
}
```


## Links

https://github.com/os-js/OS.js
