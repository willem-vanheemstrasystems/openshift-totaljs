Command Line Tools

See also https://console.preview.openshift.com/console/command-line

With the OpenShift command line interface (CLI), you can create applications and manage OpenShift projects from a terminal. You can download the oc client tool using the links below. For more information about downloading and installing it, please refer to the [Get Started with the CLI](https://docs.openshift.com/online/cli_reference/get_started_cli.html) documentation.

Download oc:

[Linux (64 bits)](https://s3.amazonaws.com/oso-preview-docker-registry/client-tools/3.4/oc-3.4.1.2-1-linux.tar.gz)

[Mac OS X](https://s3.amazonaws.com/oso-preview-docker-registry/client-tools/3.4/oc-3.4.1.2-1-macosx.tar.gz)

[Windows](https://s3.amazonaws.com/oso-preview-docker-registry/client-tools/3.4/oc-3.4.1.2-1-windows.zip)

After downloading and installing it, you can start by logging in using this current session token:

```javascript
oc login https://api.preview.openshift.com --token=...click to show token...
```

After you login to your account you will get a list of projects that you can switch between:

```javascript
oc project project-name
```

If you do not have any existing projects, you can create one:

```javascript
oc new-project project-name
```

To show a high level overview of the current project:

```javascript
oc status
```

For other information about the command line tools, check the [CLI Reference](https://docs.openshift.com/online/cli_reference/index.html) and [Basic CLI Operations](https://docs.openshift.com/online/cli_reference/basic_cli_operations.html).
