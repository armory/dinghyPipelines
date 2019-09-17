This dinghy file creates a pipeline that deploys a text based manifest and then deletes it.

What you need to replace:
Application name

For the "stage.deployManifest.module" stage
"account" set the account name defined for your cluster
"applicationName" 
"namespaceOverride" if manifest does not have a namespace defined you can override it, or just delete this line.
"textManifests" replace the namespace in there, if not using the "namespaceOverride"

For the "stage.deleteManifest.module"
"account" set the account name defined for your cluster
"location" is the namespace where the deployment happened
"mode" available options are: static, dynamic and label, each one as a separete set of options, this example uses the 3 different ones.