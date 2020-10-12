This is the source code documentation for a chrome extension Shortcuts for Chrome.

This extension is written in vanilla js with ES6 syntax; no frills or fancy stuff.

## How it Works

This extension has 3 primary parts: Popup, Menu and Background (see: [classes](list_class.html)). 

- User clicks extension icon to launch a popup. `manifest.json` specifies this behavior.

- **Popup** is a HTML template with some styling and javascript. 
    - `popup.js` will determine what visible content renders inside the popup
    - Menu is currently the only possible view, so popup will display this menu panel
      <br/><br/>

- **Menu** panel shows list of links. 
    - User can pin/unpin links and drag and drop pinned links.
    - User preferences are saved in chrome.storage, which is local to current device.
      <br/><br/>

- **Background** has no visual interface, but runs in the background of the browser
    - it manages extension context menu
    - it programmatically launches links user clicks in the menu

Beyond these 3 classes, several utility [modules](list_module.html) are used to implement this behavior.

Menu links etc. are defined in [constants](list_namespace.html).


## Development

Building this application from source requires Node.js and some web IDE.

Run these commands to build a locally debuggable version:

```
git clone https://github.com/MobileFirstLLC/shortcuts-for-chrome.git
npm install
npm run build
```

Go to `chrome://extensions` to debug the build:

1. enable developer mode
2. load unpacked > choose `dist` directory

### Available Commands

| command | description |
| --- | --- |
| `npm run start` | development build |
| `npm run build` | production build |
| `npm run docs` | generate docs |
| `npm run test` | run unit tests |
| `npm run clean` | clean generated files |
| `npm run sync` | update config files |

This extension is build with [extension-cli](https://oss.mobilefirst.me/extension-cli/).
Refer to extension-cli docs for further details on each command.

### Source Code

**[View on Github ↗](https://github.com/MobileFirstLLC/shortcuts-for-chrome)**

### Installation

**The latest release is available for installation at Chrome Web Store.**

<a href="https://chrome.google.com/webstore/detail/jnmekaomnicdcpgdndekkmojfomifjal">
<img alt="install at chrome web store" width="250" src="https://raw.githubusercontent.com/MobileFirstLLC/shortcuts-for-chrome/master/.github/badge.png"/>
</a>

* * *

**Maker:** [Mobile First](https://mobilefirst.me) &bull; **License:** [MIT](https://github.com/MobileFirstLLC/shortcuts-for-chrome/blob/master/LICENSE)