colcon-common-extensions
========================

A meta package aggregating `colcon-core <https://github.com/colcon/colcon-core>`_ as well as a set of common extensions.

Requirements for inclusion
--------------------------

As colcon's ecosystem continues to grow, the number of extensions which could possibly be considered "common" grows as well.
There are no set criteria for inclusion in this metapackage but we try to set some minimum expectations and recommendations.
Ultimately, inclusion in this metapackage will be at the discretion of the colcon core maintainers.
Removing extensions from this metapackage presents an extreme challenge since removing any package from the set of common extensions is likely to impact workflows for colcon users.
Since removal will be so difficult we must also be extremely discerning about packages that are added.

  * Included extensions must be hosted under the `colcon organization <https://github.com/colcon/>`_ on GitHub.
  * The colcon core maintainers must have the capability to make package releases through PyPI and the colcon apt repositories in the event that bugfix releases are needed and the extension's original maintainers have moved on.
  * Colcon is heavily used by the `ROS <https://ros.org/>`_ and `Gazebo <https://gazebosim.org>`_ communities.
    Adding a package to colcon-common-extensions must not adversely affect ROS 2 CI builds or Gazebo CI as ROS 2 and the ROS and Gazebo community represent a significant portion of colcon's users.
  * Packages added should depend on a minimal number of modules outside the Python standard library.
    Any package which provides features that are available using just the Python standard library must be justified.
    In order to be part of colcon-common-extensions, Python package dependencies must be available in Debian Unstable and should be available in the latest Ubuntu LTS release and in the current EPEL release.
