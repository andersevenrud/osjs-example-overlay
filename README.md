# Example OS.js overlay

This is an example "overlay" for OS.js **v2.1.x**.


The purpose of overlays like these is to completely separate your OS.js instance and any
modules, packages or client files you want to add.


## Configuration

If you clone this into your OS.js installation as `overlays/example`, place this in your custom json configuration file (ex `800-example-overlay.json`):
```json
{
  "overlays": ["overlays/example"]
}
```

This way you can for example define custom modules in your OS.js configuration. Example:

```json
{
  "authenticator": "example",
  "storage": "example",
  "themes": {
    "icons": ["default", "example"],
    "styles": ["default", "example"],
    "sounds": ["default", "example"],
    "fonts": ["Karla", "Example"]
  },
  "repositories": [
    "default",
    "example"
  ],
  "build": {
    "temlate": "example"
  }
}
```

## Links

https://github.com/os-js/OS.js
