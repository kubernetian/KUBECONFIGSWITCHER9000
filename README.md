# KubeConfigSwitcher9000 

![KUBECONFIGSWITCHER9000](mediafiles/kubeconfigswitcher9000.jpg)

Hi, I'm Joris, and I'm sick and tired of switching Kubernetes contexts. That's why 
I created this project. If you're managing multiple kubernetes clusters with an 
admin account, and you have X amount of configs in your `~/.kube/config` folder, 
use this. 

I know, there are a lot of other tools on the "OpenSource Market" but this one 
just does what it needs to do, no further bullshit. 

## How to install? 

Well that is pretty simple. 

* Clone this git 
* Put the KCS9 file in your `/usr/local/bin` folder
* Edit the permissions on the file `chmod +x /usr/local/bin/KCS9`
* `exec $SHELL` (Optional step, re-opening your terminal will do the trick as well)
* You will be able to use `KCS9` as a command from now on

