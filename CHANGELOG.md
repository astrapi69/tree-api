## Change log
----------------------

Version 1.4
-------------

ADDED:

- new method 'isAncestor' in interface ITree created that checks if a given tree node is an ancestor of this tree node
- new method 'isDescendant' in interface ITree created that checks if a given tree node is a descendant of this tree node
- new method 'move' in interface ITree created that moves a given tree node to the given new parent tree node

CHANGED:

- update gradle to new version 8.3-rc-4
- update of gradle-plugin dependency 'lombok-plugin' to new minor version 8.2.2
- update of gradle-plugin dependency 'spotless-plugin-gradle' to new minor version 6.20.0
- update of test dependency junit-jupiter-* to new minor version 5.10.0

Version 1.3
-------------

ADDED:

- new method 'isChild' in interface ITree created that checks if a given tree node is the child of this tree node

CHANGED:

- update gradle to new version 8.2-rc-2
- update of lombok version to 1.18.28
- update of gradle-plugin dependency 'spotless-plugin-gradle' to new minor version 6.19.0
- update of gradle-plugin dependency 'grgit-gradle' to new minor version 5.2.0
- javadoc optimized

Version 1.2
-------------

ADDED:

- new method 'hasPreviousSibling' in interface ITree created that checks if a node has a previous sibling
- new method 'hasNextSibling' in interface ITree created that checks if a node has a next sibling

CHANGED:

- javadoc optimized

Version 1.1
-------------

ADDED:

- new export for other modules can use ITree interface

Version 1
-------------

ADDED:

- new CHANGELOG.md file created

Notable links:
[keep a changelog](http://keepachangelog.com/en/1.0.0/) Don’t let your friends dump git logs into changelogs
