# Jump-Box
It's a single container docker image based on **Ubuntu:18.04** that can be used as a Jump-box and able to connect with any cloud K8s environment.
If you want to learn more about Jump-box then check out the following [link](https://github.com/khalfan123/jumpbox/blob/master/readme.md) of my Jump-box docker container.

> **Note:** If you need more **Packages** in jumbox kindly create an issue [here](https://github.com/khalfan123/jumpbox/issues).

### Tech

The following Packages are available and configured in Jump-Box:
* [Node v12.9.1] - Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine.
* [Azure Cli] - Set of commands used to create and manage Azure resources.
* [Helm 3.2.1] - Helm helps you manage Kubernetes applications.
* [Helm 2.14.0] - Helm helps you manage Kubernetes applications.
* [Azure Powershell] - Managing Azure resources directly from the PowerShell command line.
* [Kubectl] - Command line tool for controlling Kubernetes clusters.
* [Docker] - Package Software into Standardized Units for Development, Shipment and Deployment.
* [Docker-compose] - Compose is a tool for defining and running multi-container Docker applications.


### Installation

Jump-Box requires [Docker](https://docs.docker.com/engine/install/) to run.
Install the dependencies and start the server.

Pull the image from docker hub and run its container.

``` 
docker pull docdoc2018/jumpbox
docker run --rm -it --name jbox docdoc2018/jumpbox:latest
```
Use Volumes by running.
```
docker run --rm -it -v $(pwd):/root/Downloads --name jbox docdoc2018/jumpbox:latest
```
### Helm 2.14.0 commands
```
helm2 version --client
Client: &version.Version{SemVer:"v2.14.0", GitCommit:"05811b84a3f93603dd6c2fcfe57944dfa7ab7fd0", GitTreeState:"clean"}
```

### Helm 3.2.1 commands
```
helm version --client
version.BuildInfo{Version:"v3.2.1", GitCommit:"fe51cd1e31e6a202cba7dead9552a6d418ded79a", GitTreeState:"clean", GoVersion:"go1.13.10"}
```
### Sign in with Azure CLI
The Azure CLI's default authentication method uses a web browser and access token to sign in.
 1. Run the login command.
   ```
   az login
   ```
   If the CLI can open your default browser, it will do so and load an Azure sign-in page.

   Otherwise, open a browser page at (https://aka.ms/devicelogin) and enter the authorization code displayed in your terminal.

 2. Sign in with your account credentials in the browser.
 
 OR 

 3. [Sign in with credentials on the command line](https://docs.microsoft.com/en-us/cli/azure/authenticate-azure-cli?view=azure-cli-latest#sign-in-with-credentials-on-the-command-line) 

### Node.js Configuration
The current LTS version at the time of this writing is v12.9.1. You can upgrade or downgrade that by typing: 
```
nvm install 8.11.1

```
Usually, nvm will switch to use the most recently installed version. You can tell nvm to use the version you just downloaded by typing:
```
nvm use 8.11.1
```
When you install Node.js using nvm, the executable is called node. You can see the version currently being used by the shell by typing:
```
node -v
```
If you have multiple Node.js versions, you can see what is installed by typing:
```
nvm ls
```
If you wish to default one of the versions, type:
```
nvm alias default 8.11.1
```
This version will be automatically selected when a new session spawns. You can also reference it by the alias like this:
```
nvm use default
```

### Pre-Installed utilities
 - curl 
 - jq 
 - wget 
 - git 
 - zip 
 - unzip 

## Uninstall Docker image
If you decide to uninstall the Jump-Box, we're sorry to see you go. If you found a bug, we'd appreciate it if you file a [GitHub issue](https://github.com/khalfan123/jumpbox/issues).

```
docker rmi docdoc2018/jumpbox
```

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [Azure Cli]: <https://docs.microsoft.com/en-us/cli/azure/what-is-azure-cli?view=azure-cli-latest>
   [Helm 3.2.1]: <https://helm.sh/>
   [Helm 2.14.0]: <https://helm.sh/>
   [Azure Powershell]: <https://docs.microsoft.com/en-us/powershell/azure/?view=azps-4.2.0>
   [Kubectl]: <https://kubernetes.io/docs/tasks/tools/install-kubectl/>
   [Docker]: <https://www.docker.com/>
   [Docker-compose]: <https://docs.docker.com/compose/>
   [Node v12.9.1]: <https://helm.sh/>
 

