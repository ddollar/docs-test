---
title: "Notifications"
---

Console users can get notification for common Rack events. Below you can find a list of the types of notifications you will receive.

#### [*example-rack*] Created app *example-app*

A convox app has been created, as with `convox apps create` and is ready to accept deployments.

#### [*example-rack*] Deleted app *example-app*

A convox app has been deleted, as with `convox apps delete`.

#### [*example-rack*] Build `BNJFGEQEXOK` failed for app *example-app*

An app build failed. Run `convox builds info <id>` to view build logs.

#### [*example-rack*] Detected capacity warning

The AWS ECS service had trouble finding an available server instance on which to run one of your containers. This can be a transient error, but seeing it repeatedly can indicated that your deployment is memory- or port-constrained.

To solve this problem you can either manually scale your Rack using the `convox rack scale` command, or enable Rack autoscaling with the command `convox params set Autoscale=Yes`.

#### [*example-rack*] Rack in steady state

All of the requested processes have been successfully launched. This includes app processes and Rack processes, such as the Rack API.

#### [*example-rack*] Created release `RMDKLNZIACD` for app *example-app*

A new release has been created and is ready to be deployed. Releases are created when new builds complete or when the app’s environment variables are changed. You can promote a new release with the `convox releases promote` command.

#### [*example-rack*] Finished rolling deploy of release `RMDKLNZIACD` for app *example-app*

A deployment is totally finished. All of the new processes have been booted and all of the old processes have been stopped.

#### [*example-rack*] Promoted release `RMDKLNZIACD` for app *example-app*

A release has been promoted to be the live version on the application. This does not mean the deployment is totally complete. See the “Finished rolling deploy” notification above.

#### [*example-rack*] Scaled release `RMDKLNZIACD` for app *example-app*

A `convox scale` command has been received, instructing the Rack to run a different number of copies for a specific process.

#### [*example-rack*] Created postgres service *pg1*

A service (such as postgres, mysql, redis, etc) has been created by Convox, as with `convox services create`. This notification tells you the service type and service name, respectively.

#### [*example-rack*] Deleted postgres service *pg1*

A service has been deleted by Convox, as with `convox services delete`.

#### [*example-rack*] Updating rack to: version *20160405223647*

A rack update has been initiated. Rack updates can take from a few seconds to several minutes to complete, depending on whether they require the backing EC2 instances to be restarted. Most updates do not require instance restarts.

#### [*example-rack*] Updating rack to: count *3*

A request has been received to alter the number of instances in your Rack’s cluster. In some cases this can require processes to be re-launched and can take a few minutes to complete.

#### [*example-rack*] Updating rack to: instance type *db.t2.medium*

A request has been received to alter the type of instances in your Rack’s cluster. This will require processes to be re-launched and can take a few minutes to complete.

