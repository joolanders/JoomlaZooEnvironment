#Joomla Test environment

###General info
This package's main purpose is to provide test environment
for running unit tests for ZOOlanders projects like Framework.

###Features
This package is actual Joomla installation with installed 
YOOtheme ZOO component and plugins. 

Package also contains database
sql dump (placed within folder ```db/``` folder).

Root .htaccess, robots.txt and other files were removed as useless
for mentioned purposes. 

Also package contains bootstraping file ```joomla-env-bootstrap.php``` 
that is used to emulate Joomla application and load all necessary
classes and components for unit testing.

Configuration file ```configuration.php``` contains settings according
 to Travis CI virtual test environment. 
 
###Usage
As joomla requires database connection, you would need to
create virtual or test database and import db dump. 
Appropriate databese dump is available by path ```db/joomla.sql```.
If you use Travis CI, you can specify appropriate instructions in
your ```.travis.yml``` file.

To be able to use Joomla classes and instances, just include
```joomla-env-bootstrap.php``` file in your test bootstraping file.

*If you need for some custom joomla configuration, that is 
possible with symlinks in theory, but not realised in current package version*