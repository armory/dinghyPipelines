This dinghy file creates a simple pipeline to see the check preconditions stage.
This will check that the number of pods deployed for an application is atleast 1, if not, the pipeline will stop, and continue otherwise.

What you need to replace:
Application name
"preconditions" you need to set a deployment on your cluster, and add a precondition.

The other stages can be left as they are.