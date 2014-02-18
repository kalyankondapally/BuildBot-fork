BuildBot-fork
=============

Dependencies:
1) cython

now we can clone Ozone-Wayland build infrastructure and fetch all the dependencies of it, including Chromium build infrastructure:
gclient config ssh://git@github.com/kalyankondapally/BuildBot-fork.git --name=src/masters/master.chromium.ozonewayland --git-deps

