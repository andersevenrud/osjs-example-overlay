# Example OS.js overlay


This is an example "overlay" for OS.js (**>= v2.0.0-89**).


The purpose of overlays like these is to completely separate your OS.js instance and any
modules, packages or client files you want to add.


## Configuration

If you clone this into your OS.js installation as `overlays/example`, place this in your custom json configuration file (ex `800-example-overlay.json`):
```json
{
  "server": {
    "overlays": {
      "example": {
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

This way you can for example define custom modules (ex `801-my-settings.json`):

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

**Note: You can use absolute paths as well**

## Links

https://github.com/os-js/OS.js
