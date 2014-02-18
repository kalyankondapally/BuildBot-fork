BuildBot-fork
=============

## Contents

  - [Dependencies](#dependencies) - the architecture behind
  - [Howto](#howto) - set up the system environment, build and run
  - [License](#license)

## Dependencies:

Ensure the following dependencies are installed on your system:
  ```
1) cython
  ```

## Howto
now we can clone Ozone-Wayland build infrastructure and fetch all the dependencies of it, including Chromium build infrastructure:

  ```
gclient config ssh://git@github.com/kalyankondapally/BuildBot-fork.git --name=src/masters/master.chromium.ozonewayland --git-deps

  ```
  
## License

Ozone-Wayland CI code uses the BSD license (check the LICENSE file in the project).

