# Xe IWA TLDraw Desktop POC

This repo is a proof of concept for the idea of a web based desktop built using controlledframe and TLDraw. It is a based on the chrome controlled frame test app but modified to add a page with a desktop like view that loads multiple controlled frame windows within TLDraw.  

## Run Chrome with the right flags (simple manual method)

Some of the features you'll be trying are still under development and only
available with a particular configuration setting. Configure Chrome to prepare
for running the demo 'test_app' application.

Navigate to chrome://flags, and enable the following Experiments:
  1. enable-isolated-web-apps
  1. enable-isolated-web-app-dev-mode
  1. enable-controlled-frame

## Run using Xe IWA Launcher (tauri helper app)

Install the https://github.com/Agent54/xe-iwa-launcher app and then use it to install and launch this IWA running in dev mode. 

### From source
1. Install JS dependencies

```sh
pnpm install
```

2. Run the server

```sh
pnpm run dev
```

3. Navigate to chrome://web-app-internals, and enter the following URL into the
"Install IWA via Dev Mode Proxy" field:
```
http://localhost:5193
```

4. Launch the Controlled Frame test app

In Chrome/Chromium, you should see the demo app in chrome://apps. Click on it
to launch the IWA.
