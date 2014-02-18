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

  ```
cd src/

  ```

Create site_config/.bot_password text file with a password on one line for your slave to serve to be able to connect to the master.
  ```
echo Bleh > site_config/.bot_password

  ```

Now, we are ready to start the master.

  ```
cd src/masters/master.chromium.ozonewayland
master restart

  ...

Open another terminal and cd to src/slave

  ```
cd src/slave
TESTING_MASTER_HOST=localhost TESTING_MASTER=ChromiumOZONEWAYLAND TESTING_SLAVENAME=vm841-m1 make restart

  ...

One can start the desired slave (TESTING_SLAVENAME) defined in masters/master.chromium.ozonewayland/slave.cfg

Once you have started both the master and a slave, browse to the waterfall: http://localhost:8011/waterfall

## License

Ozone-Wayland CI code uses the BSD license (check the LICENSE file in the project).

