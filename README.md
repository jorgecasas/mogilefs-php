# MogileFS.php
## Controller for accessing Mogile File System

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

* **More info**: ITERNOVA [http://www.iternova.net]
* **Based on**: https://github.com/ash2k/mogilefs-php-client-improved


### Example 

```php
Usage Example:
// Load handler controller
$mfs = new MogileFS( 'iternova', 'assets', 'tcp://127.0.0.1' );


// Set file
$mfs->set_file( 'file_key', 'file_name.png' );

// Set data
$mfs->set( 'data_key', 'data' );

// Data exists?
echo "Data exists? " . ( $mfs->exists( 'data_key' ) ? 'YES' : 'NO' );

// Get data
echo "Get data: " . $mfs->get( 'data_key' );

// Rename key
echo "Rename data: " . $mfs->rename( 'data_key', 'new_key' );

// Delete data
$mfs->delete( 'new_key' );

// Get devices and status
$array_devices = $mfs->call_method( 'get_devices' );
print_r( $array_devices );
```

### Composer.json

In order to use composer (and packagist.org), complete your composer.json file with:

```js
{
    "require": {
       "jorgecasas/mogilefs-php": "dev-master"
    }
}
```

