Improved classmap autoloader
===========================

Usage
-----

```
php classmap_generator.php -l [directory]
```

Generates classmap with shorter variables and without spaces. That may improve performance for very big classmaps (like the one generated for Zend Framework - it's more than 300kB in size!). Also makes it possible to ignore certain prefixes when generating the classmap. That can also improve performance in some cases.

Ignoring some class prefixes
-----------------------------

Create a file named ".classmapIgnore.php" in the directory (you can use the example file from this repository) and list the prefixes in an array, that is returned. Note, that it's full prefix - including namespace. So you can exclude complete namespaces too. 