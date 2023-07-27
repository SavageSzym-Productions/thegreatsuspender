# The Great Suspender - Easy to use Tab Manager

<img src="/src/img/suspendy-guy.png" width="100px" />


### Build from github

Dependencies: openssl, npm.

Clone the repository and run these commands:
```
npm install
npm run generate-key
npm run build
```

It should say:
```
Done, without errors.
```

The extension in crx format will be inside the build/crx/ directory. You can drag it into [extensions] (chrome://extensions) to install locally.

### Integrating with another Chrome extension or app

This extension has a small external api to allow other extensions to request the suspension of a tab. See [this issue](https://github.com/greatsuspender/thegreatsuspender/issues/276) for more information. And please let me know about it so that I can try it out!

### Windows Group Policies

It is possible to force settings by defining group policies on Microsoft
Windows.

The whitelist is stored internally as a string, with one URL per line.

The following settings can be defined:

* `SCREEN_CAPTURE` (string, default: '0')
* `SCREEN_CAPTURE_FORCE` (boolean, default: false)
* `SUSPEND_IN_PLACE_OF_DISCARD` (boolean, default: false)
* `DISCARD_IN_PLACE_OF_SUSPEND` (boolean, default: false)
* `USE_ALT_SCREEN_CAPTURE_LIB` (boolean, default: false)
* `DISCARD_AFTER_SUSPEND` (boolean, default: false)
* `IGNORE_WHEN_OFFLINE` (boolean, default: false)
* `IGNORE_WHEN_CHARGING` (boolean, default: false)
* `UNSUSPEND_ON_FOCUS` (boolean, default: false)
* `IGNORE_PINNED` (boolean, default: true)
* `IGNORE_FORMS` (boolean, default: true)
* `IGNORE_AUDIO` (boolean, default: true)
* `IGNORE_ACTIVE_TABS` (boolean, default: true)
* `IGNORE_CACHE` (boolean, default: false)
* `ADD_CONTEXT` (boolean, default: true)
* `SYNC_SETTINGS` (boolean, default: true)
* `SUSPEND_TIME` (string (minutes), default: '60')
* `NO_NAG` (boolean, default: false)
* `WHITELIST` (string (one URL per line), default: '')
* `THEME` (string, default: 'light')

### Contributing to this extension

Contributions are very welcome. Feel free to submit pull requests for new features and bug fixes. For new features, ideally you would raise an issue for the proposed change first so that we can discuss ideas. This will go a long way to ensuring your pull request is accepted.
