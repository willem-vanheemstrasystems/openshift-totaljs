#Instructions

##Create an account with Redhat - OpenShift Online (Next Gen)

See for documentation: https://docs.openshift.com/online/welcome/index.html

##OpenShift Online

Open the OpenShift Console by following this link after having signed in with your OpenShift Online (Next Gen) User Account.

https://console.preview.openshift.com/console/

The first time you will see a 'Welcome to OpenShift.' message and a button to create a New Project.

###New Project

Click the 'New Project' button on the console (as mentioned above) to create a new project.

When asked, answer the following questions:

***Name***: Give a unique name for the project, e.g. totaljs-001

***Display Name***: Give the name as it will be displayed, e.g. TotalJS - 001

***Description***: Give a description of the project, e.g. A TotalJS Project (001)

Follow by clicking the 'Create' button

Next, on the 'Browse Catalog' tab, choose from a web framework. Here fill in 'node' in the filter text input field.

You will be given (at least) two options:

- Node.js  <-- Choose this one
- Node.js + MongoDB (Persistent)

Choose Node.js ( Builds source code. Build and run Node.js 4 applications on RHEL 7. For more information about using this builder image, including OpenShift considerations, https://github.com/sclorg/s2i-nodejs-container/blob/master/4/README.md ) 

Choose the latest version (i.e. 4 -- latest at the time of this writing).

Confirm by clicking the 'Select' button.
___

You will be shown the following:

Node.js

Build and run Node.js 4 applications on RHEL 7. For more information about using this builder image, including OpenShift considerations, see https://github.com/sclorg/s2i-nodejs-container/blob/master/4/README.md.

Version: 4

***Name***: Give a name, e.g. totaljs-001-nodejs-4

***Git Repository URL***: Give the repository for the nodejs application, here https://github.com/willem-vanheemstrasystems/openshift-totaljs.git

Show advanced routing, build, deployment and source options by clicking the link with the same name.

It will show the following:

***Git Reference***: master
Optional branch, tag, or commit.

***Context Dir***: /
Optional subdirectory for the application source code, used as the context directory for the build.

***Source Secret***: Secret name ( we will leave this blank for the moment )
Secret with credentials for pulling your source code. 

The option to 'Create new secret'. We will not do so now.

##Routing

Routing is a way to make your application publicly visible. Otherwise you may only be able to access your application by its IP address, if allowed by the system administrator.

Create a route to the application

***Hostname***: www.example.com ( We will leave this blank for now )
Public hostname for the route. If not specified, a hostname is generated. The hostname can't be changed after the route is created.

***Path***: /
Path that the router watches to route traffic to the service.

***Target Port***: 8080/TCP
Target port for traffic

[Optional] Secure route (leave unchecked for now)
routes can be secured using several TLS termination types for serving certificates.

##Build configuration

A build configuration describes how to build your deployable image. This includes your source, the base builder image, and when to launch new builds.

[Checked] Configure a webhook build trigger
[Checked] Automatically build a new image when the builder image changes
[Checked] Launch the first build when the build configuration is created

Environment Variables (Build and Runtime)

Environment variables are used to configure and pass information to running containers. These environment variables will be available during your build and at runtime.

[Optional] ***name***  ***value*** (leave blank for now)
___

##Deployment Configuration

Deployment configurations describe how your application is configured by the cluster and under what conditions it should be recreated (e.g. when the image changes).

Autodeply when
[Checked] New image is available
[Checked] Deployment configuration changes

Environment Variables (Runtime only)

Environment variables are used to configure and pass information to running containers. These environment variables will only be available at runtime.

These variables exist on the image and will be available at runtime. You may override them below.

***PATH***: /opt/app-root/src/node_modules/.bin/:/opt/app-root/src/.npm-global/bin/:/opt/app-root/src/bin:/opt/app-root/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

***container***: docker

***STI_SCRIPTS_URL***: image:///usr/libexec/s2i

***STI_SCRIPTS_PATH***: /usr/libexec/s2i

***HOME***: /opt/app-root/src

***BASH_ENV***: /opt/app-root/etc/scl_enable

***ENV***: /opt/app-root/etc/scl_enable

***PROMPT_COMMAND***: . /opt/app-root/etc/scl_enable

***NODEJS_VERSION***: 4

***NPM_RUN***: start

***NPM_CONFIG_PREFIX***: /opt/app-root/src/.npm-global

[Optional] ***name***  ***value*** (leave blank for now)

___

##Scaling










