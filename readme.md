# @beyond-js/module-loaders

`@beyond-js/module-loaders` is a utility library that provides a simple wrapper around RequireJS and SystemJS, enabling
these popular module loaders to be used as ES modules. By default, RequireJS and SystemJS are not compatible with modern
JavaScript module systems, but this library addresses that limitation.

## Features

-   **Modular Usage**: Use RequireJS and SystemJS as ES modules.
-   **Simple Integration**: Easily integrate these legacy module loaders in your projects.
-   **Improved Compatibility**: Overcome issues related to loading and managing modules in different environments.

## Installation

Install the package via npm:

```bash
npm install @beyond-js/module-loaders
```

Or using yarn:

```bash
yarn add @beyond-js/module-loaders
```

## Usage

To use RequireJS and SystemJS as modules in your project, import them as follows:

```javascript
import requirejs from '@beyond-js/module-loaders/vendor/require.min.js';
import systemjs from '@beyond-js/module-loaders/vendor/s.js';

// Example usage with RequireJS
requirejs(['moduleA', 'moduleB'], function (moduleA, moduleB) {
	// Your logic here
});

// Example usage with SystemJS
systemjs.import('/path/to/your/module.js').then(module => {
	// Your logic here
});
```

### Why Use This Wrapper?

By default, RequireJS and SystemJS are designed as global script loaders and don’t support being imported as ES modules.
This library wraps these loaders, allowing them to be used seamlessly within modern JavaScript module systems.

## Folder Structure

The key files in this package are:

```
module-loaders/
│
├── vendor/
│   ├── require.min.js       # RequireJS library
│   └── s.js                 # SystemJS library
├── package.json
└── README.md                # Documentation
```

-   **`vendor/require.min.js`**: Minified version of RequireJS.
-   **`vendor/s.js`**: SystemJS library.

## Contributing

Contributions are welcome! Please follow the [contributing guidelines](CONTRIBUTING.md) if you wish to contribute.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This `README.md` gives an overview of the package, explains its purpose, and provides usage instructions. If you need
more details added or modifications, feel free to ask!
