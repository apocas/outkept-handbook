# Introduction

The idea behind `Outkept` was to build a tool that could be able to auto-discover your cluster profile and simultaneously start monitoring and controlling each node it finds.

`Outkept` does not have any hardcoded behavior, instead what it haves is a pool of available sensors and stabilization/reactive action for each sensor. When it finds a new server in one of the monitorized subnets, it looks for supported sensors by running a verifier command (ex. mysql exists? in a mysql thread number sensors).

If you have a heterogeneous cluster constantly changing, `Outkept` allows you to easily automate control behavior and cluster monitorization.
