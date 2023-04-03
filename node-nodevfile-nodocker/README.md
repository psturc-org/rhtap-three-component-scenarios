Component without devfile or docker used for testing RHTAP multi component

![Node.js CI](https://github.com/nodeshift-starters/nodejs-health-check/workflows/ci/badge.svg)
[![Coverage Status](https://coveralls.io/repos/github/nodeshift-starters/nodejs-health-check/badge.svg?branch=main)](https://coveralls.io/github/nodeshift-starters/nodejs-health-check?branch=main)

Example Health Check Application

## Running The Example

You can run this example as node processes on your localhost, as pods on a local
[OpenShift Local](https://developers.redhat.com/products/openshift-local/overview) installation.

### Localhost

To run the basic application on your local machine, just run the commands bellow:

```
$ npm install
$ npm start
```

This will launch the application on port 8080.

Other options:

* `npm run dev` same as `npm start` but with pretty output log.
* `npm run dev:debug` shows debug information.

### OpenShift Local

OpenShift Local should be started, and you should be logged in with a currently
active project. Then run the `npm run openshift` command.

```sh
$ crc setup # Set-up the hypervisor
$ crc start # Initialize the openshift cluster
$ oc login -u developer # Login
$ oc new-project my-example-project # Create a project to deploy to
$ npm run openshift # Deploys the example app
```

### OpenTelemetry with OpenShift Distributed Tracing Platform

This [link](./OTEL.md) contains instructions on how to install the
OpenShift Distributed Tracing Platform and enable tracing.