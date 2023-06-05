# Overview

This is NOT a stand alone demo.
This is a repo to hold the Helm Chart for another demo

See https://github.com/tplatt37/a-new-startup-eks-cicd 

This chart is used specifically by a CI/CD Pipeline. It differs from the chart I use to do manual deployments.
Biggest difference - this chart ALWAYS uses a service account.

## Test after making changes!

You can run the following to "test" your Chart:
```
helm lint a-new-startup
```

This is like a dry-run with no actual attempted install.
```
helm template a-new-startup --namespace test
```

## Spinnaker demo

If deploying with a Spinnaker Bake Manifest stage, a tar.gz is required.

You can create this with:
```
helm package a-new-startup
```
The output file will be named a-new-startup-1.0.0.tgz

