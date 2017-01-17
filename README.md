Java gRPC plugin
==

## Plugin overview

This repository provides a sample [gRPC](http://www.grpc.io/) plugin, written in Java, intended to work as part of [Tyk](https://tyk.io/). Maven is used.

A simple request dispatcher is implemented, based on [Tyk custom middleware hooks](https://tyk.io/docs/tyk-api-gateway-v1-9/javascript-plugins/middleware-scripting/) logic.
A class implements the required hook methods.

## Running the gRPC server

To run:

```
$ mvn exec:java -Dexec.mainClass="com.tyktechnologies.tykmiddleware.TykMiddleware"
```

## Building a plugin bundle

The [`manifest.json`](manifest.json) file describes the hooks implemented by this plugin, to use it you must generate a bundle and load it into your Tyk API settings, [this guide](https://tyk.io/tyk-documentation/customise-tyk/plugins/rich-plugins/plugin-bundles/) will walk you through the process.

