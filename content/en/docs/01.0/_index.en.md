---
title: "1. Getting started"
weight: 1
sectionnumber: 1
description: >
  Get familiar with the lab environment.
---


## Task {{% param sectionnumber %}}.1: Login

The first thing we're going to do is to explore our lab environment and get in touch with the different components.

Login into the web console of the Lab Cluster with the provided Username and Password.

{{% alert title="Note" color="primary" %}} Ask your trainer if you don't have your Cluster-URL or Username and Password {{% /alert %}}

The project with your username is going to be used for all the hands-on labs.


### Task {{% param sectionnumber %}}.1.1: Web IDE

{{% alert title="Note" color="primary" %}}ALPHA: you can also use you local installation of the cli tools.{{% /alert %}}

As your lab environment, we use a so-called web IDE, directly deployed on the lab environment. To login to your specific web IDE, we need to figure out the IDE Password, which is configured as Environment Variable in the Deployment `amm-techlab-ide` in your project.

Go and get the value out of the Environment Variable and log into the Web IDE.

{{% alert title="Note" color="primary" %}}Use Chrome for the best experience. The Url to the Web IDE also can be found in your project. The deployment is exposed with a route. {{% /alert %}}


Once you're successfully logged into the web IDE open a new Terminal by hitting `CTRL + SHIFT + C` or clicking the Menu button --> Terminal --> new Terminal and check the installed oc version by executing the following command:

```bash
oc version
```

The Web IDE Pod consists of the following tools:

* oc
* kubectl
* kustomize
* helm
* kubectx
* kubens
* tekton cli
* odo
* argocd

The files in the home directory under `/home/coder` are stored in a persistence volume.


### Task {{% param sectionnumber %}}.1.2: Login with oc tool

The easiest way to login to the lab cluster using the oc tool is, by copying the login command from the web console (Click on the Username in the top right corner of your web console and then Copy Login Command, to get to the login command).

Paste this login command in the Terminal and verify the output `Logged into...`.

Switch to your project with `oc project <username>`

If you want to use your local `oc` tool, make sure to get the appropriate version.


### Task {{% param sectionnumber %}}.1.3: explore other namespaces

Alongside the Lab Cluster, we also deployed a couple of additional Tools and Services we're going to use during the lab.

checkout the Deployed resources and then Login into the services. (URLs are provided by the trainer)

* Git Server `pitc-infra-gitea`, this will contain the source code (Login with your username and password)
* Prometheus and Grafana in the project `pitc-infra-apps-monitoring` (Login using Oauth OpenShift)
* ArgoCD in the project `pitc-infra-argocd` (Login via OpenShift)
