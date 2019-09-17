This dinghy file creates a pipeline for a bake deploy strategy
This will bake a helm chart and then deploy the manifest.

What you need to replace:
Application name
"expectedArtifacts" section, replace the reference and type object (you can create the artifact on the ui and just copy/paste the object in here)

For the "stage.bakeManifest.module" 
"namespace" is important to replace to the namespace you are going to deploy to.
"inputArtifacts" the id of this needs to match the id from the `expectedArtifacts` section above in this example the id is `myChartFromS3`
"expectedArtifacts" this id needs to match the id on the next section.


For the "stage.deployManifest.module"
"account" is the kubernetes account configured on your halConfig
"namespaceOverride" set this up if you want to override the namespace to another one.