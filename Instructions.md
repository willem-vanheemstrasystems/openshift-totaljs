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


