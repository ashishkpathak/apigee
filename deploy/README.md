
`apigeetool` is a Node.js module and you can install it using npm:

`npm install -g apigeetool`

_NOTE_: The `-g` option places the apigeetool command in your PATH. On "*nix"-based machines, `sudo` may be required with the `-g` option. If you do not use `-g`, then you need to add the apigeetool command to your PATH manually. Typically, the `-g` option places modules in: `/usr/local/lib/node_modules/apigee-127` on *nix-based machines.

# What you need to know about apigeetool

You must have an account on Apigee Edge to perform any `apigeetool` functions. These functions include:

-   deploying an API proxy or shared flow to Edge,
-   undeploying an API proxy or shared flow from Edge,
-   deploying Node.js apps to Edge,
-   listing deployed API proxies or shared flows on Edge,
-   retrieving deployed proxies or shared flows from Edge,
-   deleting proxy or shared flow definitions from Edge, and
-   retreiving log messages from Node.js apps deployed to Edge.
-   create or delete an API product in Edge
-   create or delete a Developer in Edge
-   create or delete a Developer Application in Edge
-   create or delete a Cache resource in Edge
-   create, retrieve or delete a KVM Map in Edge
-   create, retrieve or delete a KVM Entry in Edge
-   attach, detach, or get a FlowHook
-   create, get, delete, list Target Servers
-   create, get, delete, List Roles
-   get, set Role Permisions
-   assign, remove, verify Users for a Role
-   list all Users in a Role

You need to be familiar with basic concepts and features of Apigee Edge such as API proxies, organizations, and environments.

For more information, refer to the [Apigee Edge docs](http://apigee.com/docs/).

# Common Parameters

The following parameters are available on all of the commands supported by this tool:

`--baseuri -L` (optional) The base URI for you organization on Apigee Edge. The default is the base URI for Apigee cloud deployments is `api.enterprise.apigee.com`. For on-premise deployments, the base URL may be different.

`--header -H` (optional) Adds a header to the API call. Format is header:value. This option may be used multiple times if more than one header is needed.

`--cafile -c` (optional) The names of one of more PEM files that represent trusted certificate authorities. Multiple file names may be comma-separated. Use this to communicate with an installation of Apigee Edge that uses a custom certificate for API calls.

`--keyfile -K` (optional) The name of the PEM file that represents the private key in a mutual auth connection.

`--certfile -C` (optional) The name of the PEM file that represents the certificate in a mutual auth connection.

`--debug -D` (optional) Prints additional information about the deployment, including router and message processor IDs.

`--help -h` (optional) Displays help on this command.

`--insecure -k` (optional) Do not validate the TLS certificate of the HTTPS target for API calls. Use this to communicate with an installation of Apigee Edge that does not use a trusted TLS certificate.

`--asynclimit -a` (optional) Limit for the maximum number of operations performed concurrently. Currently this only affects file uploads in the `deploynodeapp` command. Defaults to 4.

`--json -j` (optional) Formats the command's response as a JSON object.

`--organization -o` (required) The name of the organization to deploy to. May be set as an environment variable APIGEE_ORGANIZATION.

`--password -p` (required) Your Apigee account password. May be set as an environment variable APIGEE_PASSWORD.

`--username -u` (required) Your Apigee account username. May be set as an environment variable APIGEE_USERNAME.

`--token -t` (optional) Your Apigee access token. Use this in lieu of -u / -p

`--netrc -N` (optional) Use this in lieu of -u / -p, to tell apigeetool to retrieve credentials from your .netrc file.

`--verbose -V` (optional) Prints additional information as the deployment proceeds.

# Command reference and examples

-   [addEntryToKVM](https://www.npmjs.com/package/apigeetool#addEntryToKVM)
-   [assignUserRole](https://www.npmjs.com/package/apigeetool#assignUserRole)
-   [attachFlowHook](https://www.npmjs.com/package/apigeetool#attachFlowHook)
-   [createappkey](https://www.npmjs.com/package/apigeetool#createappkey)
-   [createapp](https://www.npmjs.com/package/apigeetool#createapp)
-   [createcache](https://www.npmjs.com/package/apigeetool#createcache)
-   [createdeveloper](https://www.npmjs.com/package/apigeetool#createdeveloper)
-   [createKVMmap](https://www.npmjs.com/package/apigeetool#createKVMmap)
-   [createProduct](https://www.npmjs.com/package/apigeetool#createproduct)
-   [createRole](https://www.npmjs.com/package/apigeetool#createRole)
-   [createTargetServer](https://www.npmjs.com/package/apigeetool#createTargetServer)
-   [deleteapp](https://www.npmjs.com/package/apigeetool#deleteapp)
-   [deletecache](https://www.npmjs.com/package/apigeetool#deletecache)
-   [deletedeveloper](https://www.npmjs.com/package/apigeetool#deletedeveloper)
-   [deleteKVMentry](https://www.npmjs.com/package/apigeetool#deleteKVMentry)
-   [deleteKVMmap](https://www.npmjs.com/package/apigeetool#deleteKVMmap)
-   [deleteproduct](https://www.npmjs.com/package/apigeetool#deleteproduct)
-   [deleteRole](https://www.npmjs.com/package/apigeetool#deleteRole)
-   [deleteSharedflow](https://www.npmjs.com/package/apigeetool#deleteSharedflow)
-   [deleteTargetServer](https://www.npmjs.com/package/apigeetool#deleteTargetServer)
-   [delete](https://www.npmjs.com/package/apigeetool#delete)
-   [deployhostedtarget](https://www.npmjs.com/package/apigeetool#deployhostedtarget)
-   [deploynodeapp](https://www.npmjs.com/package/apigeetool#deploynodeapp)
-   [deployproxy](https://www.npmjs.com/package/apigeetool#deployproxy)
-   [deploySharedflow](https://www.npmjs.com/package/apigeetool#deploySharedflow)
-   [detachFlowHook](https://www.npmjs.com/package/apigeetool#detachFlowHook)
-   [fetchproxy](https://www.npmjs.com/package/apigeetool#fetchproxy)
-   [fetchSharedflow](https://www.npmjs.com/package/apigeetool#fetchSharedflow)
-   [getFlowHook](https://www.npmjs.com/package/apigeetool#getFlowHook)
-   [getKVMentry](https://www.npmjs.com/package/apigeetool#getKVMentry)
-   [getKVMmap](https://www.npmjs.com/package/apigeetool#getKVMmap)
-   [getlogs](https://www.npmjs.com/package/apigeetool#getlogs)
-   [getRole](https://www.npmjs.com/package/apigeetool#getRole)
-   [getRolePermissions](https://www.npmjs.com/package/apigeetool#getRolePermissions)
-   [getTargetServer](https://www.npmjs.com/package/apigeetool#getTargetServer)
-   [listdeployments](https://www.npmjs.com/package/apigeetool#listdeployments)
-   [listRoles](https://www.npmjs.com/package/apigeetool#listRoles)
-   [listRoleUsers](https://www.npmjs.com/package/apigeetool#listRoleUsers)
-   [listSharedflowDeployments](https://www.npmjs.com/package/apigeetool#listSharedflowDeployments)
-   [listTargetServers](https://www.npmjs.com/package/apigeetool#listTargetServers)
-   [removeUserRole](https://www.npmjs.com/package/apigeetool#removeUserRole)
-   [setRolePermissions](https://www.npmjs.com/package/apigeetool#setRolePermissions)
-   [undeploySharedflow](https://www.npmjs.com/package/apigeetool#undeploySharedflow)
-   [undeploy](https://www.npmjs.com/package/apigeetool#undeploy)
-   [updateKVMEntry](https://www.npmjs.com/package/apigeetool#updateKVMEntry)
-   [updateTargetServer](https://www.npmjs.com/package/apigeetool#updateTargetServer)
-   [verifyUserRole](https://www.npmjs.com/package/apigeetool#verifyUserRole)

## deploynodeapp

Deploys a Node.js app to Apigee Edge as an API proxy. With your Node.js app deployed to Edge, you can take advantage of Edge features like security, quotas, caching, analytics, trace tool, and more.

#### [](https://www.npmjs.com/package/apigeetool#examples)Examples

Deploys a Node.js app to Apigee Edge.

```
apigeetool deploynodeapp -u sdoe@apigee.com -o sdoe -e test -n 'Test Node App 2' -d . -m app.js -b /node2

```

Deploys a Node.js app to both the default (HTTP) and secure (HTTPS) virtual hosts.

```
apigeetool deploynodeapp -u sdoe@apigee.com -o sdoe -e test -n 'Test Node App 2' -d . -m app.js -b /node2 -v default,secure

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

For example, if you do not specify a password using "-p", apigeetool will prompt for the password on the command line.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--environments -e` (required) The name(s) of the environment(s) to deploy to (comma-delimited).

#### Optional parameters

`--api -n` (optional) The name of the API proxy. The name of the API proxy must be unique within an organization. The characters you are allowed to use in the name are restricted to the following: `A-Z0-9._\-$ %`. If not specified, will attempt to use name from package.json.

`--base-path -b` (optional) The base path of the API proxy. For example, for this API proxy, the base path is `/example-proxy`: `http://myorg-test.apigee.net/example-proxy/resource1`.

`--directory -d` (optional) The path to the root directory of the API proxy on your local system. Will attempt to use current directory is none is specified.

`--import-only -i` (optional) Imports the API proxy to Apigee Edge but does not deploy it.

`--main -m` (optional) The Node.js file you want to be the main file. If not specified, will attempt to use main from package.json.

`--preserve-policies -P` (optional) If specified, the highest revision of the existing proxy will be downloaded and the node code in your directory will be overlayed upon it to create a resulting proxy that contains both any existing policies and the node code in the directory. If there is no existing revision, this option will have no effect.

`--resolve-modules -R` (optional) If the API proxy includes Node.js modules (e.g., in a `node_modules` directory), this option updates them on Apigee Edge without uploading them from your system. Basically, it's like running "npm install" on Apigee Edge in the root directory of the API proxy bundle.

`--production` (optional) Indicates if Apigee Edge should use the `--production` flag during `npm install`. Defaults to `true`, example of disabling the flag would be `--production false`.

`--upload-modules -U`  
(optional) If specified, uploads Node.js modules from your system to Apigee Edge rather than resolving the modules directly on Apigee Edge (the default behavior).

`--virtualhosts -v` (optional) A comma-separated list of virtual hosts that the deployed app will use. The two most common options are `default` and `secure`. The `default` option is always HTTP and `secure` is always HTTPS. By default, `apigeetool deploynodeapp` uses `default,secure`.

`--bundled-dependencies` (optional) If specified, the source code will be uploaded with its `bundledDependencies` as defined in the `package.json`.

`--wait-after-import -W`  
(optional) Number of seconds to delay before deploying node.js proxy.

## deployhostedtarget

Deploys a Hosted Target to Apigee Edge as an API proxy. With your Hosted Target deployed to Edge, you can take advantage of Edge features like security, quotas, caching, analytics, trace tool, and more.

#### Examples

Deploys a Node.js app as a Hosted Target to Apigee Edge.

```
apigeetool deployhostedtarget -u sdoe@apigee.com -o sdoe -e test -n 'test-node-app-2' -b /node2

```

Deploys a Node.js app as a Hosted Target to both the default (HTTP) and secure (HTTPS) virtual hosts.

```
apigeetool deployhostedtarget -u sdoe@apigee.com -o sdoe -e test -n 'test-node-app-2' -b /node2 -v default,secure

```

#### Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

For example, if you do not specify a password using "-p", apigeetool will prompt for the password on the command line.

See [Common Parameters] for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--api -n` The name of the API proxy. The name of the API proxy must be unique within an organization. The characters you are allowed to use in the name are restricted to the following: `a-z0-9._\-$ %`.

`--environments -e` (required) The name(s) of the environment(s) to deploy to (comma-delimited).

#### Optional parameters

`--base-path -b` (optional) The base path of the API proxy. For example, for this API proxy, the base path is `/example-proxy`: `http://myorg-test.apigee.net/example-proxy/resource1`.

`--directory -d` (optional) The path to the root directory of the API proxy on your local system. Will attempt to use current directory is none is specified.

`--import-only -i` (optional) Imports the API proxy to Apigee Edge but does not deploy it.

`--preserve-policies -P` (optional) If specified, the highest revision of the existing proxy will be downloaded and the source code in your directory will be overlayed upon it to create a resulting proxy that contains both any existing policies and the source code in the directory. If there is no existing revision, this option will have no effect.

`--virtualhosts -v` (optional) A comma-separated list of virtual hosts that the deployed app will use. The two most common options are `default` and `secure`. The `default` option is always HTTP and `secure` is always HTTPS. By default, `apigeetool deployhostedtarget` uses `default,secure`.

`--bundled-dependencies` (optional) If specified, the source code will be uploaded with its `bundledDependencies` as defined in the `package.json`.

## deployproxy

Deploys an API proxy to Apigee Edge. If the proxy is currently deployed, it will be undeployed first, and the newly deployed proxy's revision number is incremented.

#### Example

Deploys an API proxy called example-proxy to Apigee Edge. Per the `-d` flag, the command is executed in the root directory of the proxy bundle.

```
apigeetool deployproxy  -u sdoe@example.com -o sdoe  -e test -n example-proxy -d .

```

#### Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters] for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--api -n` (required) The name of the API proxy. Note: The name of the API proxy must be unique within an organization. The characters you are allowed to use in the name are restricted to the following: `A-Z0-9._\-$ %`.

`--environments -e` (required) The name(s) of the environment(s) to deploy to (comma delimited).

#### Optional parameters

`--base-path -b` (optional) The base path of the API proxy. For example, for this API proxy, the base path is /example-proxy: [http://myorg-test.apigee.net/example-proxy/resource1](http://myorg-test.apigee.net/example-proxy/resource1).

`--directory -d` (optional) The path to the root directory of the API proxy on your local system. Will attempt to use current directory is none is specified.

`--import-only -i` (optional) Imports the API proxy to Apigee Edge but does not deploy it.

`--resolve-modules -R` (optional) If the API proxy includes Node.js modules (e.g., in a `node_modules` directory), this option updates them on Apigee Edge without uploading them from your system. Basically, it's like running npm on Apigee Edge in the root directory of the API proxy bundle.

`--upload-modules -U` (optional) If specified, uploads Node.js modules from your system to Apigee Edge.

`--bundled-dependencies` (optional) If specified, the `node` & `hosted` resources will be uploaded with their `bundledDependencies` as defined in their respective `package.json` files.

`--wait-after-import -W`  
(optional) Number of seconds to delay before deploying node.js proxy.

## deployExistingRevision

Deploys an existing API proxy revision to Apigee Edge. If a different revision is already deployed to the targeted environments, it will be undeployed and replaced with the requested revision.

#### Example

Deploys an existing API proxy revision called example-proxy to Apigee Edge.

```
apigeetool deployExistingRevision  -u sdoe@example.com -o sdoe  -e test -n example-proxy -r 1

```

#### Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--api -n`  
(required) The name of the API proxy. Note: The name of the API proxy must be unique within an organization. The characters you are allowed to use in the name are restricted to the following: `A-Z0-9._\-$ %`.

`--environments -e`  
(required) The name(s) of the environment(s) to deploy to (comma delimited).

`--revision -r` (required) The existing revision of the proxy to be deployed.

## undeploy

Undeploys a named API proxy or Node.js app deployed on Apigee Edge.

#### Example

Undeploy the proxy named "example-proxy".

```
apigeetool undeploy -u sdoe@example.com -o sdoe  -n example-proxy -e test -D

```

#### Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--api -n` (required) The name of the API proxy or app to undeploy.

`--environment -e` (required) The environment on Apigee Edge where the API proxy or app is currently deployed.

#### Optional parameters

`--revision -r` (optional) Specify the revision number of the API proxy to undeploy.

## listdeployments

Lists the API proxies deployed on Apigee Edge for the specified organization. Lets you filter the result by API proxy name or environment.

#### Examples

List all API proxies in an organization:

```
$ apigeetool listdeployments -u sdoe@example.com -o sdoe -e test`

```

List API proxies named "example-proxy":

```
$ apigeetool listdeployments -u sdoe@example.com -o sdoe -n example-proxy

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-5)Required parameters

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

#### [](https://www.npmjs.com/package/apigeetool#required-mutually-exclusive-parameters)Required, mutually exclusive parameters

`--api -n` (You must specify either `api` or `environment` in this command) The name of the API proxy to list.

`--environment -e` (You must specify either `api` or `environment` in this command) The environment for which you want to list deployments. When `-e` is specified, the command lists all deployed proxies in the environment.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-4)Optional parameters

`--long -l` (optional) Returns additional information about the API proxy or Node.js app, including the URL to use as the base path for each one.

`--revision -r` (optional) Filters the list by the specified revision number.

## [](https://www.npmjs.com/package/apigeetool#fetchproxy)fetchproxy

Fetches a deployed API proxy or Node.js application from Apigee Edge. The result will be a ZIP file that contains the contents of the entire proxy.

Regardless of whether "deployproxy" or "deploynodeapp" is used to deploy the proxy or app, the result of "fetchproxy" will always be a ZIP file that represents an API proxy. The resulting proxy may be "unzipped" and re-deployed using "deployproxy."

#### [](https://www.npmjs.com/package/apigeetool#example-3)Example

Fetch the deployed proxy named "example-proxy".

```
apigeetool fetchproxy -u sdoe@example.com -o sdoe -n example-proxy -r 1

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-6)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--api -n` (required) The name of the API proxy or app to undeploy.

`--revision -r` (required) Specifies the revision to retrieve.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-5)Optional parameters

`--file -f` (optional) The name of the file to write as the result. If not specified, then the file name will be the same as the name passed to the "name" parameter.

## [](https://www.npmjs.com/package/apigeetool#delete)delete

Delete all revisions of a proxy from Apigee Edge.

It is an error to delete a proxy that still has deployed revisions. Revisions must be undeployed using "undeploy" before this command may be used.

#### [](https://www.npmjs.com/package/apigeetool#example-4)Example

Delete the proxy named "example-proxy".

```
apigeetool delete -u sdoe@example.com -o sdoe -n example-proxy

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-7)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--api -n` (required) The name of the API proxy or app to undeploy.

## [](https://www.npmjs.com/package/apigeetool#getlogs)getlogs

Retrieve the last set of log records from a Node.js application or Hosted Target deployed to Apigee Edge.

The resulting log files will be written directly to standard output. Each is prefixed with:

-   A timestamp, in UTC by default
-   An indication of whether the log record came from standard output or standard error
-   A unique identifier of the server where the log was generated.

Since Apigee Edge, by default, deploys each Node.js application on at least two different servers, most applications will see at least two sets of logs. These are sorted in time stamp order.

The log records from this command come from a cache inside Apigee Edge that retains the last 500 lines of log output from each server. The cache is a circular buffer, so older messages will be discarded when it fills up.

By default, the last set of log records will be pulled and written to standard output. However, if the "-f" option is used, then "apigeetool" will poll Edge for new log records and append them to standard output, in the manner of "tail -f". (By default, the tool polls every five seconds).

For example, a set of log records might look like this:

[2014-11-05T01:30:01.530Z nodejs/stderr svr.362] *** Starting script
[2014-11-05T01:30:09.182Z nodejs/stderr svr.362] 2014-11-05T01:30:09.181Z - debug: 1/4. this is a debug log
[2014-11-05T01:30:09.186Z nodejs/stdout svr.362] 2014-11-05T01:30:09.186Z - info: 2/4. this is an info log
[2014-11-05T01:30:09.187Z nodejs/stdout svr.362] 2014-11-05T01:30:09.187Z - warn: 3/4. this is a warning log
[2014-11-05T01:30:09.188Z nodejs/stderr svr.362] 2014-11-05T01:30:09.188Z - error: 4/4. this is an error log
[2014-11-05T01:48:21.419Z nodejs/stderr svr.828] *** Starting script
[2014-11-05T01:48:28.637Z nodejs/stderr svr.828] js-bson: Failed to load c++ bson extension, using pure JS version
[2014-11-05T01:48:29.801Z nodejs/stderr svr.828] 2014-11-05T01:48:29.800Z - debug: 1/4. this is a debug log
[2014-11-05T01:48:29.804Z nodejs/stdout svr.828] 2014-11-05T01:48:29.804Z - info: 2/4. this is an info log
[2014-11-05T01:48:29.805Z nodejs/stdout svr.828] 2014-11-05T01:48:29.805Z - warn: 3/4. this is a warning log
[2014-11-05T01:48:29.806Z nodejs/stderr svr.828] 2014-11-05T01:48:29.806Z - error: 4/4. this is an error log

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-8)Required Parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--api -n` (required) The name of the deployed app to get logs from.

`--environment -e` (required) The environment on Apigee Edge where the app is currently deployed.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-6)Optional Parameters

`--streaming -f` (optional) If specified, do not exit, but instead poll Apigee Edge for new log records and write them to standard output in the manner of "tail -f."

`--timezone -z` (optional) If specified, use the time zone to format the timestamps on the log records. If not specified, then the default is UTC. The timestamp name should be a name such as "PST."

`--hosted-build` (optional) If specified will attempt to get the build logs for a deployed Hosted Target.

`--hosted-runtime` (optional) If specified will attempt to get the runtime logs for a deployed Hosted Target.

## [](https://www.npmjs.com/package/apigeetool#deploysharedflow)deploySharedflow

Deploys a sharedFlow to Apigee Edge. If the sharedFlow is currently deployed, it will be undeployed first, and the newly deployed sharedflow's revision number is incremented.

#### [](https://www.npmjs.com/package/apigeetool#example-5)Example

Deploys a SharedFlow called example-sf to Apigee Edge. Per the `-d` flag, the command is executed in the root directory of the sharedflow bundle.

```
apigeetool deploySharedflow  -u sdoe@example.com -o sdoe  -e test -n example-sf -d .

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-9)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--name -n` (required) The name of the SharedFlow. Note: The name of the SharedFlow must be unique within an organization. The characters you are allowed to use in the name are restricted to the following: `A-Z0-9._\-$ %`.

`--environments -e` (required) The name(s) of the environment(s) to deploy to (comma delimited).

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-7)Optional parameters

`--directory -d` (optional) The path to the root directory of the sharedflow on your local system. Will attempt to use current directory is none is specified.

`--import-only -i` (optional) Imports the sharedflow to Apigee Edge but does not deploy it.

## [](https://www.npmjs.com/package/apigeetool#undeploysharedflow)undeploySharedflow

Undeploys a SharedFlow deployed on Apigee Edge.

#### [](https://www.npmjs.com/package/apigeetool#example-6)Example

Undeploy the proxy named "example-sf".

```
apigeetool undeploySharedflow -u sdoe@example.com -o sdoe  -n example-sf -e test -D

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-10)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--name -n` (required) The name of the sharedflow to undeploy.

`--environment -e` (required) The environment on Apigee Edge where the sharedflow is currently deployed.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-8)Optional parameters

`--revision -r` (optional) Specify the revision number of the sharedflow to undeploy.

## [](https://www.npmjs.com/package/apigeetool#listsharedflowdeployments)listSharedflowDeployments

Lists the sharedflows deployed on Apigee Edge for the specified organization. Lets you filter the result by API proxy name or environment.

#### [](https://www.npmjs.com/package/apigeetool#examples-3)Examples

List all Sharedflows in an organization:

```
$ apigeetool listSharedflowDeployments -u sdoe@example.com -o sdoe -e test` #Won't work due to missing API

```

List Sharedflows named "example-sf":

```
$ apigeetool listSharedflowDeployments -u sdoe@example.com -o sdoe -n example-sf

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-11)Required parameters

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

#### [](https://www.npmjs.com/package/apigeetool#required-mutually-exclusive-parameters-1)Required, mutually exclusive parameters

`--name -n` (You must specify either `name` or `environment` in this command) The name of the Sharedflow to list.

`--environment -e` (You must specify either `name` or `environment` in this command) The environment for which you want to list deployments. When `-e` is specified, the command lists all deployed proxies in the environment.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-9)Optional parameters

`--revision -r` (optional) Filters the list by the specified revision number.

## [](https://www.npmjs.com/package/apigeetool#fetchsharedflow)fetchSharedFlow

Fetches a sharedFlow from Apigee Edge. The result will be a ZIP file that contains the contents of the entire sharedflow.The resulting ZIP file may be "unzipped" and re-deployed using "deploySharedflow."

#### [](https://www.npmjs.com/package/apigeetool#example-7)Example

Fetch the deployed proxy named "example-proxy".

```
apigeetool fetchSharedflow -u sdoe@example.com -o sdoe -n example-proxy -r 1

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-12)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--name -n` (required) The name of the sharedflow or app to undeploy.

`--revision -r` (required) Specifies the revision to retrieve.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-10)Optional parameters

`--file -f` (optional) The name of the file to write as the result. If not specified, then the file name will be the same as the name passed to the "name" parameter.

## [](https://www.npmjs.com/package/apigeetool#deletesharedflow)deleteSharedflow

Delete all revisions of a sharedflow from Apigee Edge.

It is an error to delete a proxy that still has deployed revisions. Revisions must be undeployed using "undeploySharedflow" before this command may be used.

#### [](https://www.npmjs.com/package/apigeetool#example-8)Example

Delete the proxy named "example-sf".

```
apigeetool deleteSharedflow -u sdoe@example.com -o sdoe -n example-sf

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-13)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--name -n` (required) The name of the API proxy or app to undeploy.

## [](https://www.npmjs.com/package/apigeetool#kvm-operations)KVM Operations

The following commands support the varying scoped of the Apigee KVM.

When just the `--organization` option is present, the operation will correspond to the Organization-scoped KVM.

When the `--organization` and `--environment` options are present, the operation will correspond to the Environment-scoped KVM.

When the `--organization` and `--api` options are present, the operation will correspond to the API-scoped KVM.

### [](https://www.npmjs.com/package/apigeetool#createkvmmap)createKVMmap

Creates a map in the Apigee KVM with the given name.

#### [](https://www.npmjs.com/package/apigeetool#example-9)Example

Create KVM map named "test-map"

```
apigeetool createKVMmap -u sdoe@example.com -o sdoe -e test --mapName test-map

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-14)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--mapName` (required) The name of the map to be created.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-11)Optional parameters

`--environment -e` (optional) The environment to target for an Environment-scoped KVM operation.

`--api -n` (optional) The API to target for an API-scoped KVM operation.

`--encrypted` (optional) Create a encrypted KVM Map.

### [](https://www.npmjs.com/package/apigeetool#addentrytokvm)addEntryToKVM

Adds an entry of name:value to the named map in the Apigee KVM.

#### [](https://www.npmjs.com/package/apigeetool#example-10)Example

Add entry to KVM with name "test1" and value "value1"

```
apigeetool addEntryToKVM -u sdoe@example.com -o sdoe -e test --mapName test-map --entryName test1 --entryValue value1

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-15)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--mapName` (required) The name of the map the entry will belong to.

`--entryName` (required) The name of the entry to be created.

`--entryValue` (required) The value of the entry to be created.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-12)Optional parameters

`--environment -e` (optional) The environment to target for an Environment-scoped KVM operation.

`--api -n` (optional) The API to target for an API-scoped KVM operation.

### [](https://www.npmjs.com/package/apigeetool#updatekvmentry)updateKVMEntry

Updates an entry of name:value to the named map in the Apigee KVM.

#### [](https://www.npmjs.com/package/apigeetool#example-11)Example

Update entry to KVM with name "test1" and value "value1"

```
apigeetool updateKVMentry -u sdoe@example.com -o sdoe -e test --mapName test-map --entryName test1 --entryValue value1

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-16)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--mapName` (required) The name of the map the entry will belong to.

`--entryName` (required) The name of the entry to be created.

`--entryValue` (required) The value of the entry to be created.

`--environment -e` (optional) The environment to target for an Environment-scoped KVM operation.

### [](https://www.npmjs.com/package/apigeetool#getkvmmap)getKVMmap

Retrieves an entire KVM map with all of its entries, by name.

#### [](https://www.npmjs.com/package/apigeetool#example-12)Example

Get map named "test-map".

```
apigeetool getKVMmap -u sdoe@example.com -o sdoe -e test --mapName test-map

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-17)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--mapName` (required) The name of the map to be retrieved.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-13)Optional parameters

`--environment -e` (optional) The environment to target for an Environment-scoped KVM operation.

`--api -n` (optional) The API to target for an API-scoped KVM operation.

### [](https://www.npmjs.com/package/apigeetool#getkvmentry)getKVMentry

Retrieve an unencrypted KVM entry from an Apigee KVM map, by name.

#### [](https://www.npmjs.com/package/apigeetool#example-13)Example

Retrieve the KVM entry named "test1" in the map "test-map".

```
apigeetool getKVMentry -u sdoe@example.com -o sdoe -e test --mapName test-map --entryName test1

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-18)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--mapName` (required) The name of the map that the entry belongs to.

`--entryName` (required) The name of the entry to be retrieved.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-14)Optional parameters

`--environment -e` (optional) The environment to target for an Environment-scoped KVM operation.

`--api -n` (optional) The API to target for an API-scoped KVM operation.

### [](https://www.npmjs.com/package/apigeetool#deletekvmmap)deleteKVMmap

Deletes an entire map from the Apigee KVM along with all of its entries.

#### [](https://www.npmjs.com/package/apigeetool#example-14)Example

Delete map named "test-map".

```
apigeetool deleteKVMmap -u sdoe@example.com -o sdoe -e test --mapName test-map

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-19)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--mapName` (required) The name of the map to be deleted.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-15)Optional parameters

`--environment -e` (optional) The environment to target for an Environment-scoped KVM operation.

`--api -n` (optional) The API to target for an API-scoped KVM operation.

### [](https://www.npmjs.com/package/apigeetool#deletekvmentry)deleteKVMentry

Deletes a single entry by name from an Apigee KVM map.

#### [](https://www.npmjs.com/package/apigeetool#example-15)Example

Delete entry named "test1" from the map named "test-map".

```
apigeetool deleteKVMmmap -u sdoe@example.com -o sdoe -e test --mapName test-map --entryName test1

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-20)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`--mapName` (required) The name of the map that the entry belongs to.

`--entryName` (required) The name of the entry to be deleted.

#### [](https://www.npmjs.com/package/apigeetool#optional-parameters-16)Optional parameters

`--environment -e` (optional) The environment to target for an Environment-scoped KVM operation.

`--api -n` (optional) The API to target for an API-scoped KVM operation.

## [](https://www.npmjs.com/package/apigeetool#cache-operations)Cache Operations

### [](https://www.npmjs.com/package/apigeetool#createcache)createcache

Creates a Cache with the given name.

#### [](https://www.npmjs.com/package/apigeetool#example-16)Example

Create Cache map named "test-cache"

```
apigeetool createcache -u sdoe@example.com -o sdoe -e test -z test-cache 

```

Create Cache map named "test-cache" (with description and expiry)

```
apigeetool createcache -u sdoe@example.com -o sdoe -e test -z test-cache --description "sample key" --cacheExpiryInSecs 40000    

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-21)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password, and the "-o" parameter for organization name, all of which are required.

`-z` (required) The name of the cache to be created.

`--environment -e` (required) The environment to target.

`--description` (optional) The description of the cache to be created.

`--cacheExpiryByDate` (optional) Date by which the cache will expire. Date format must be mm-dd-yyyy.

`--cacheExpiryInSecs` (optional) Duration in seconds by which the cache will expire.

## [](https://www.npmjs.com/package/apigeetool#target-server-operations)Target Server Operations

### [](https://www.npmjs.com/package/apigeetool#createtargetserver)createTargetServer

Creates a Target Server with the given name.

#### [](https://www.npmjs.com/package/apigeetool#example-17)Example

Create Target Server named "test-target" with SSL enabled.

```
apigeetool createTargetServer -N -o $ORG -e $ENV --targetServerName test-target --targetHost httpbin.org --targetPort 443 --targetSSL true

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-22)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.  
`--targetServerName` (required) The name of the Target Server to be created.  
`--targetHost` (required) The hostname of the target.  
`--targetPort` (required) The port number of the target.  
`--targetSSL` (optional) Whether or not SSL is configured, defaults to none.  
`--targetEnabled` (optional) Whether or not the Target Server itself is enabled, defaults to true.

### [](https://www.npmjs.com/package/apigeetool#updatetargetserver)updateTargetServer

Update a Target Server with the given name.

#### [](https://www.npmjs.com/package/apigeetool#example-18)Example

Update Target Server named "test-target" with SSL enabled.

```
apigeetool updateTargetServer -N -o $ORG -e $ENV --targetServerName test-target --targetHost httpbin.org --targetPort 443 --targetSSL true

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-23)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.  
`--targetServerName` (required) The name of the Target Server to be created.  
`--targetHost` (required) The hostname of the target.  
`--targetPort` (required) The port number of the target.  
`--targetSSL` (optional) Whether or not SSL is configured, defaults to none.  
`--targetEnabled` (optional) Whether or not the Target Server itself is enabled, defaults to true.

### [](https://www.npmjs.com/package/apigeetool#deletetargetserver)deleteTargetServer

Deletes a Target Server with the given name.

#### [](https://www.npmjs.com/package/apigeetool#example-19)Example

Delete Target Server named "test-target".

```
apigeetool deleteTargetServer -N -o $ORG -e $ENV --targetServerName test-target

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-24)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.  
`--targetServerName` (required) The name of the Target Server to be deleted.

### [](https://www.npmjs.com/package/apigeetool#gettargetserver)getTargetServer

Get details for a Target Server with the given name.

#### [](https://www.npmjs.com/package/apigeetool#example-20)Example

Get Target Server named "test-target".

```
apigeetool getTargetServer -N -o $ORG -e $ENV --targetServerName test-target

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-25)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.  
`--targetServerName` (required) The name of the Target Server to be deleted.

### [](https://www.npmjs.com/package/apigeetool#listtargetservers)listTargetServers

List Target Servers in a given environment.

#### [](https://www.npmjs.com/package/apigeetool#example-21)Example

List Target Servers.

```
apigeetool listTargetServers -N -o $ORG -e $ENV

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-26)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.

## [](https://www.npmjs.com/package/apigeetool#flowhook-operations)FlowHook Operations

Operations on the pre-defined FlowHook names:

-   PreProxyFlowHook
-   PreTargetFlowHook
-   PostTargetFlowHook
-   PostProxyFlowHook

### [](https://www.npmjs.com/package/apigeetool#attachflowhook)attachFlowHook

Attach a deployed SharedFlow to one of the [named FlowHooks](#FlowHook Operations).

#### [](https://www.npmjs.com/package/apigeetool#example-22)Example

Attach SharedFlow "GetLogValues" to "PreProxyFlowHook".

```
apigeetool attachFlowHook -N -o $ORG -e $ENV --flowHookName PreProxyFlowHook --sharedFlowName GetLogValues

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-27)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.  
`--flowHookName` (required) The pre-defined name of the FlowHook.  
`--sharedFlowName` (required) The name of a deployed SharedFlow.

### [](https://www.npmjs.com/package/apigeetool#detachflowhook)detachFlowHook

Detach a SharedFlow from one of the [named FlowHooks](#FlowHook Operations).

#### [](https://www.npmjs.com/package/apigeetool#example-23)Example

Detach "PreProxyFlowHook".

```
apigeetool detachFlowHook -N -o $ORG -e $ENV --flowHookName PreProxyFlowHook

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-28)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.  
`--flowHookName` (required) The pre-defined name of the FlowHook.

### [](https://www.npmjs.com/package/apigeetool#getflowhook)getFlowHook

Get the SharedFlow currently attached to one of the [named FlowHooks](#FlowHook Operations).

#### [](https://www.npmjs.com/package/apigeetool#example-24)Example

Detach "PreProxyFlowHook".

```
apigeetool getFlowHook -N -o $ORG -e $ENV --flowHookName PreProxyFlowHook

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-29)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--environment -e` (required) The environment to target.  
`--flowHookName` (required) The pre-defined name of the FlowHook.

## [](https://www.npmjs.com/package/apigeetool#roles-and-permissions-operations)Roles and Permissions Operations

Operations on Roles, Permissions and User assignment. The general flow is:

-   Create a role
-   Assign Permissions to the Role
-   Assign the Role to a User

### [](https://www.npmjs.com/package/apigeetool#createrole)createRole

Create a role.

#### [](https://www.npmjs.com/package/apigeetool#example-25)Example

Create role "AllowGetUserRoles".

```
apigeetool createRole -N -o $ORG --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-30)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--roleName` (required) The name for the role.

### [](https://www.npmjs.com/package/apigeetool#getrole)getRole

Get a role.

#### [](https://www.npmjs.com/package/apigeetool#example-26)Example

Get role "AllowGetUserRoles".

```
apigeetool getRole -N -o $ORG --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-31)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--roleName` (required) The name for the role.

### [](https://www.npmjs.com/package/apigeetool#deleterole)deleteRole

Delete a role.

#### [](https://www.npmjs.com/package/apigeetool#example-27)Example

Delete role "AllowGetUserRoles".

```
apigeetool deleteRole -N -o $ORG --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-32)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--roleName` (required) The name for the role.

### [](https://www.npmjs.com/package/apigeetool#listroles)listRoles

List roles.

#### [](https://www.npmjs.com/package/apigeetool#example-28)Example

List roles.

```
apigeetool listRoles -N -o $ORG

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-33)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.

### [](https://www.npmjs.com/package/apigeetool#setrolepermissions)setRolePermissions

Set Role Permissions for a Role.

#### [](https://www.npmjs.com/package/apigeetool#example-29)Example

Set Permissions on Role "AllowGetUserRoles" to allow access to list Roles.

```
apigeetool setRolePermissions -N -o $ORG --roleName AllowGetUserRoles --permissions '[{"path":"/userroles","permissions":["get"]}]'

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-34)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--roleName` (required) The name for the role.  
`--permissions` Permissions array for path and verbs.

### [](https://www.npmjs.com/package/apigeetool#getrolepermissions)getRolePermissions

Get Role Permissions for a Role.

#### [](https://www.npmjs.com/package/apigeetool#example-30)Example

Get Permissions on Role "AllowGetUserRoles".

```
apigeetool getRolePermissions -N -o $ORG --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-35)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--roleName` (required) The name for the role.

### [](https://www.npmjs.com/package/apigeetool#assignuserrole)assignUserRole

Assign existing User to a Role. NOTE: User must already exist in Edge.

#### [](https://www.npmjs.com/package/apigeetool#example-31)Example

Assign "[somedeveloper@any.com](mailto:somedeveloper@any.com)" to Role "AllowGetUserRoles".

```
apigeetool assignUserRole -N -o $ORG --email "somedeveloper@any.com" --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-36)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--email` (required) Email for an existing User in Edge.  
`--roleName` (required) The name for the role.

### [](https://www.npmjs.com/package/apigeetool#removeuserrole)removeUserRole

Remove existing User from a Role.

#### [](https://www.npmjs.com/package/apigeetool#example-32)Example

Remove "[somedeveloper@any.com](mailto:somedeveloper@any.com)" from Role "AllowGetUserRoles".

```
apigeetool removeUserRole -N -o $ORG --email "somedeveloper@any.com" --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-37)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--email` (required) Email for an existing User in Edge.  
`--roleName` (required) The name for the role.

### [](https://www.npmjs.com/package/apigeetool#verifyuserrole)verifyUserRole

Verify User assigned to a Role.

#### [](https://www.npmjs.com/package/apigeetool#example-33)Example

Verify "[somedeveloper@any.com](mailto:somedeveloper@any.com)" assigned to Role "AllowGetUserRoles".

```
apigeetool verifyUserRole -N -o $ORG --email "somedeveloper@any.com" --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-38)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--email` (required) Email for an existing User in Edge.  
`--roleName` (required) The name for the role.

### [](https://www.npmjs.com/package/apigeetool#listroleusers)listRoleUsers

Get Users assigned to a Role.

#### [](https://www.npmjs.com/package/apigeetool#example-34)Example

List Users assigned to Role "AllowGetUserRoles".

```
apigeetool listRoleUsers -N -o $ORG --roleName AllowGetUserRoles

```

#### [](https://www.npmjs.com/package/apigeetool#required-parameters-39)Required parameters

The following parameters are required. However, if any are left unspecified on the command line, and if apigeetool is running in an interactive shell, then apigeetool will prompt for them.

See [Common Parameters](https://www.npmjs.com/package/apigeetool#commonargs) for a list of additional parameters, including the "-u" and "-p" parameters for username and password or preferably -N for .netrc usage.

`--organization -o` (required) The organization to target.  
`--email` (required) Email for an existing User in Edge.  
`--roleName` (required) The name for the role.

# [](https://www.npmjs.com/package/apigeetool#sdk-reference)SDK Reference

You could use apigeetool as an SDK to orchestrate tasks that you want to perform with Edge, for eg, deploying an api proxy or running tests etc.

#### [](https://www.npmjs.com/package/apigeetool#usage-example)Usage Example

```
var apigeetool = require('apigeetool')
var sdk = apigeetool.getPromiseSDK()
var opts = {
    organization: 'edge-org',
    username: 'edge-user',
    password: 'password',
    environments: 'environment',
}
opts.api = APIGEE_PROXY_NAME;
opts.directory = path.join(__dirname);

sdk.deployProxy(opts)
    .then(function(result){
        //deploy success
    },function(err){
        //deploy failed
    });

```

## [](https://www.npmjs.com/package/apigeetool#create-developer)Create Developer

Creates a new Developer in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-35)Example

Create a developer.

```
    //see above for other required options
    opts.email = DEVELOPER_EMAIL
opts.firstName = 'Test'
opts.lastName = 'Test1'
opts.userName = 'runningFromTest123'
opts.attributes = [
    {
        name: "testAttribute",
        value: "newValue"
    }
]

sdk.createDeveloper(opts)
  .then(function(result){
    //developer created
  },function(err){
    //developer creation failed
  }) ;

```

## [](https://www.npmjs.com/package/apigeetool#delete-developer)Delete Developer

Delete a Developer in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-36)Example

```
    //see above for other required options
    opts.email = DEVELOPER_EMAIL

sdk.deleteDeveloper(opts)
  .then(function(result){
    //developer deleted
  },function(err){
    //developer delete failed
  }) ;

```

## [](https://www.npmjs.com/package/apigeetool#create-product)Create Product

Creates a new API Product in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-37)Example

```
opts.productName = APIGEE_PRODUCT_NAME
opts.productDesc = 'description'
opts.proxies = APIGEE_PROXY_NAME
opts.environments = 'test' //apigee env
opts.quota = '1', //quota amount
opts.quotaInterval = '1' //interval
opts.quotaTimeUnit = 'minute' //timeunit

sdk.createProduct(opts)
  .then(function(result){
    //product created
  },function(err){
    //product creation failed
  }) ;

```

## [](https://www.npmjs.com/package/apigeetool#delete-product)Delete Product

Delete API Product in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-38)Example

```
opts.productName = APIGEE_PRODUCT_NAME

sdk.deleteProduct(opts)
  .then(function(result){
    //delete success
  },function(err){
    //delete failed
  }) ;

```

## [](https://www.npmjs.com/package/apigeetool#create-app)Create App

Create App in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-39)Example

```
  opts.name = APP_NAME
  opts.apiproducts = APIGEE_PRODUCT_NAME
  opts.email = DEVELOPER_EMAIL

  sdk.createApp(opts)
  .then(function(result){
    //create app done
  },function(err){
    //create app failed
  }) ;

```

## [](https://www.npmjs.com/package/apigeetool#delete-app)Delete App

Delete App in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-40)Example

```
  opts.email = DEVELOPER_EMAIL
  opts.name = APP_NAME

  sdk.deleteApp(opts)
  .then(function(result){
    //delete app success
  },function(err){
    //delete app failed
  }) ;

```

## [](https://www.npmjs.com/package/apigeetool#create-app-key)Create App Key

Create App Key in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-41)Example

```
opts.key = APP_KEY;
opts.secret = APP_SECRET;
opts.developerId = DEVELOPER_EMAIL;
opts.appName = APP_NAME;
opts.apiProducts = PRODUCT_NAME;

sdk.createAppKey(opts)
.then(function(result){
//create key/secret success
},function(err){
//create key/secret failed
}) ;

```

## [](https://www.npmjs.com/package/apigeetool#create-cache)Create Cache

Create Cache in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-42)Example

```
opts.cache = CACHE_RESOURCE_NAME;
sdk.createcache(opts)
.then(function(result){
    //cache create success
  },function(err){
    //cache create failed
  }) ;

```

## [](https://www.npmjs.com/package/apigeetool#delete-cache)Delete Cache

Delete Cache in Edge

#### [](https://www.npmjs.com/package/apigeetool#example-43)Example

```
opts.cache = CACHE_RESOURCE_NAME;
sdk.deletecache(opts)
.then(function(result){
    //delete create success
  },function(err){
    //delete create failed
  }) ;

```

# [](https://www.npmjs.com/package/apigeetool#original-tool)Original Tool

This module replaces the original "apigeetool," which was written in Python. It is also called "apigeetool" and resides here:

[https://github.com/apigee/api-platform-tools](https://github.com/apigee/api-platform-tools)

# [](https://www.npmjs.com/package/apigeetool#contribution)Contribution

To run remotetests, provide your edge creds, org, env details in `remotetest/testconfig.js` similar to 'remotetest/testconfig-sample.js'

