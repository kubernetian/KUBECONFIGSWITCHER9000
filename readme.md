# KubeConfigSwitcher9000 

![KUBECONFIGSWITCHER9000](mediafiles/kubeconfigswitcher9000.jpg)

# Table of contents

  1. [Introduction](#introduction)
  2. [Prerequisites](#prerequisites)
  3. [How to install?](#how-to-install)
  4. [Example](#example)

# Introduction

Hi, I'm Joris and I'm sick and tired of switching kubernetes contexts. That's why 
I created this project. If you're managing multiple kubernetes clusters with an 
admin account and you have X amount of configs in your `~/.kube/config` folder 
use this. 

I know, there are a lot of other tools on the "OpenSource Market" but this one 
just does what it needs to do, no further bullshit. 

# Prerequisites 

Be sure you have a named copy of your kubeconfig in your `~/.kube` folder. For 
example :

        user@ubuntu:~# ls -l 
                kube1_config
                kube2_config
                kube3_config
                config

> :warning: **Lost kubeconfigs are not my responsibility.**


# How to install? 

Well that is pretty simple. 

* Clone this git 
* Put the KCS9 file in your `/usr/local/bin` folder
* Edit the permissions on the file `chmod +x /usr/local/bin/KCS9`
* `exec $SHELL` (Optional step, re-opening your terminal will do the trick as well) 
* You will be able to use `KCS9` as a command from now on

## Debian

Since the v0.0.2 release there is a debian package available. Find the package 
on the releases page and install it with the following command : 

        dpkg -i KCS9.deb

## ARCH

There is an AUR package available called `kcs9-git`. Install with your favourite AUR helper!

# Example 

        user@ubuntu:~# KCS9
        1) kube1_config
        2) kube2_config
        3) kube3_config
        Which config do you want to use? 2
        Selected config: kube2_config
        user@ubuntu:~# cat .kube/config
        this is the kube2 config
        user@ubuntu:~# KCS9
        1) kube1_config
        2) kube2_config
        3) kube3_config
        Which config do you want to use? 1
        Selected config: kube1_config
        user@ubuntu:~# cat .kube/config
        this is the kube1 config
        user@ubuntu:~# KCS9
        1) kube1_config
        2) kube2_config
        3) kube3_config
        Which config do you want to use? 3
        Selected config: kube3_config
        user@ubuntu:~# cat .kube/config
        this is the kube3 config
