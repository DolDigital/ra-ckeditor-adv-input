# ra-ckeditor-adv-input

### CKEditor5 and Monaco editor for react-admin

## Installation
This package requires an SVG loader so setup your environment accordingly.
If you use CRA this package comes with a bundles configuration for @craco/craco

**Add the package**

```yarn add @doldigital/ra-ckeditor-adv-input```

**Install craco**

```yarn add @craco/craco```

**Create craco.config.js in CRA root**
```
const { enableCKEWebpackConfigPlugin } = require('./src/ra-ckeditor-adv-input/lib/craco.config')
module.exports = {
  webpack: {
    alias: {},
    plugins: [],
    configure: (webpackConfig, { env, paths }) => {
      return enableCKEWebpackConfigPlugin(webpackConfig, { env, paths });
    }
  }
};
```

**Alter package.json to use craco instead of react-scripts**
```
...
  "scripts": {
    "start": "craco start",
    "build": "craco build",
    "test": "craco test",
    "eject": "react-scripts eject"
  },
...
```

## Usage
