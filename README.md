# NoSleep.js

Prevent display sleep and enable wake lock in all Android and iOS web browsers.

Check out the [live demo](https://mikahayk.github.io/NoSleep/run) in a web browser.

## Usage
Import ES6 module:

```javascript
import NoSleep from 'nosleep.js';
```

Create a new NoSleep object and then enable or disable it when needed.

To create a new NoSleep object:

```javascript
var noSleep = new NoSleep();
```

To enable wake lock:

**NOTE: This function call must be wrapped in a user input event handler e.g. a mouse or touch handler**

```javascript
// Enable wake lock.
// (must be wrapped in a user input event handler e.g. a mouse or touch handler)
document.addEventListener('click', function enableNoSleep() {
  document.removeEventListener('click', enableNoSleep, false);
  noSleep.enable();
}, false);
```

To disable wake lock:

```javascript
// Disable wake lock at some point in the future.
// (does not need to be wrapped in any user input event handler)
noSleep.disable();
```

## License

MIT. Copyright (c) [Rich Tibbett](https://twitter.com/_richtr).

See the [LICENSE](https://github.com/richtr/NoSleep.js/blob/master/LICENSE) file.
