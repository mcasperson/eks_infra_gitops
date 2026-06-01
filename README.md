# Directory Structure

* `apps` contains Kubernetes resources or Argo CD Applications deploying Helm charts
  * `apps/<app name>` contains the resources for an application
    *  `apps/<app name>/base` contains the environment agnostic application configuration
    *  `apps/<app name>/template` contains the templates used by Octopus to update the application
    *  `apps/<app name>/envs/<environment name>` contains the Kustomize overlays for the base application
* `rootapps` contains Argo CD Applications deploying the resources in `apps`