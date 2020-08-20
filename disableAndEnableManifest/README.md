This dinghy file creates a pipeline to showcase the disable and enable Stages.
It first deploys a simple cronjob that prints "Hello from the Kubernetes cluster", then disables it, enables it again, and then deletes it.

What you need to replace:
Application name

For the "stage.deployManifest.module" stage
"account" set the account name defined for your cluster
"applicationName" 
"namespaceOverride" if manifest does not have a namespace defined you can override it, or just delete this line.
"textManifests" replace the namespace in there, if not using the "namespaceOverride"

For the "stage.disableManifest.module" and  "stage.enableManifest.module"
"account" set the account name defined for your cluster
"app" applicationName
"namespace" the namespace


For the "stage.deleteManifest.module"
"account" set the account name defined for your cluster
"namespace" is the namespace where the deployment happened
"mode" available options are: static, dynamic and label, each one as a separete set of options, this example uses the 3 different ones.
