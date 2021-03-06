loklak webclient
=====================================

Web client for loklak server (see: https://github.com/loklak/loklak_server ).
To use the loklak webclient, you need a running loklak server. Install and run it first.

---

### Dev

1. Clone this repo from `https://github.com/loklak/loklak_webclient.git`
2. Create your custom settings file by using `cp configFile.json custom_configFile.json`. Edit your settings inside `custom_configFile.json`.
3. Run `npm install` from the root directory
4. Run `gulp dev` (may require installing Gulp globally `npm install gulp -g`)
5. Your browser will automatically be opened and directed to the browser-sync proxy address
6. To prepare assets for production, run the `gulp prod` task (Note: the production task does not fire up the express server, and won't provide you with browser-sync's live reloading. Simply use `gulp dev` during development. More information below)

Now that `gulp dev` is running, the server is up as well and serving files from the `/build` directory. Any changes in the `/app` directory will be automatically processed by Gulp and the changes will be injected to any open browsers pointed at the proxy address.

### Config

Set the apiUrl var in `custom_configFile.json` to set the server address in `apiUrl`

### Troubleshooting

- On *nix based systems (latest Ubuntu, Fedora version) you might get an `Error: watch ENOSPC` when running `gulp dev`. To fix, check [this post](http://stackoverflow.com/questions/16748737/grunt-watch-error-waiting-fatal-error-watch-enospc) on Stackoverflow. 
