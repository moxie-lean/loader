#Loader

> Allows to load files from directories with a more sugared syntax, and
> allowing the use of params passed to the fils.


# Register directories where to look for file.

```php
add_filter( 'loader_directories', function( $directories ){
  $directories[] = get_template_directory();
  return $directories;
});
```

That will search files on the root directory of your theme.


# Register alias

The alias are used to search inside of directories more easily for
example:  

```php
add_filter('loader_alias', function( $alias ){
  $alias['partial'] = 'partials';
  return $alias;
});
```

Which give us a sintax like this: 

```php
Load::partial( 'button' );
```
