# Pristine PHP

![Pristine PHP logo](logo.jpg)

Collection of useful PHP functions and code snippets.

<!-- TOC -->

- [Pristine PHP](#pristine-php)
    - [Advanced string Interpolation](#advanced-string-interpolation)
    - [Casting](#casting)
    - [Folder exists](#folder-exists)
    - [JSON to class](#json-to-class)
    - [One time file download](#one-time-file-download)

<!-- /TOC -->

## Advanced string Interpolation

> Source: https://stackoverflow.com/a/15410466/13604898

```php
function identity(mixed $arg): mixed {
    return $arg;
}
$interpolate = "identity";

echo "<input value='{$interpolate(1 + 1 * random_int())}' />";
```

## Casting

See [Casting.php](Casting.php)

## Folder exists

```php
/**
 * Checks if a folder exist and return canonicalized absolute pathname (sort version)
 * @param string $folder the path being checked.
 * @return mixed returns the canonicalized absolute pathname on success otherwise FALSE is returned
 */
function folder_exist(string $folder): string|false
{
    // Get canonicalized absolute pathname
    $path = realpath($folder);

    // If it exist, check if it's a directory
    return ($path !== false AND is_dir($path)) ? $path : false;
}
```

## JSON to class

See [JSON2Class.php](JSON2Class.php)

## One time file download

See [OnetimeFileDownload.php](OnetimeFileDownload.php)
