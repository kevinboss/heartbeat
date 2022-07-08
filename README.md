# heartbeat

## What is it

Is that repo dead, is the mantainer still responding to issues? Can I safely use this dependency?

Sometimes something hasn't been abandoned, it is just complete or doesn't need a lot of maintenance. How do you communicate to your users that you are still here? Hearbeats aim is to provide a way to signal that a maintainer is still here while not creating unnecessary features or just empy commits.

## How to use it

Add a yaml file in ./hearts to configure your repo. Heartbeat will ask you to send a signal (a beat) whenever the last beat has been long ago.
