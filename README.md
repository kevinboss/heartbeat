# heartbeat

## What is it

Is that repo dead, is the maintainer still responding to issues? Can I safely use this dependency?

Sometimes something hasn't been abandoned, it is just complete or doesn't need a lot of maintenance. How do you communicate to your users that you are still here? Hearbeats aim is to provide a way to signal that a maintainer is still here while not creating unnecessary features or just empy commits.

## How to use it

Add a yaml file in ./hearts to configure your repo.

Hearbeat will check your repo for the latest commit date. If that date has been more than 30 days ago heartbeat will ask you to provide a beat. Whenever you commit to your repo or provide a beat heartbeat will save that date as your latest beat.

Heartbeat will then generate a badge in the badges folder that you can display in your repository. Add a link to this repo to provide context.
