# Server Requirements Checker
This script can help before installing an application by checking for common required modules to be enabled on the server.

![Preview](https://raw.githubusercontent.com/ParadoxalManiak/server-requirements-checker/master/preview.png)

### Features
 - Check for PHP version
 - Check for cURL, JSON, MCrypt, mbstring, GD, BC Math, MySQLi, PDO and sockets support
 - Check if PEAR is installed
 - Check if directory is writable
 - Clean coded and easy to understand
 - Small size
 - Base64 encoded images
 - Single-file script
 - Easy configuration

### Installation
    1. Download or clone this repository
    2. Open check.php with your favourite code editor and edit the configuration (see below)
    3. Upload check.php to the desired web server and access the file using http://www.your-domain.com/check.php

### Configuration
Open check.php in your favourite code editor and find the following block of code. Read the comments for more info.
```php
 /**
 * #######################################
 *  Configuration
 * #######################################
 */

$requirements = new stdClass();

// PHP Version selection
$requirements->phpMin = '5.6.0';
$requirements->phpMax = '7.0.9';

// Check for cURL support ?
$requirements->curl = true;

// Check for JSON support ?
$requirements->json = true;

// Check for MCrypt support ?
$requirements->mcrypt = true;

// Check for mbstring support ?
$requirements->mbstring = true;

// Check if PEAR is installed ?
$requirements->pear = true;

// Write permission check
$requirements->writeCheck = true;
$requirements->writeDir   = __DIR__;

// GD Support check
$requirements->gdCheck    = true;
$requirements->gdShowMore = true; // Show more details about gd ?

// Check for BC Math support ?
$requirements->bcmath = true;

// Check for MySQLi support ?
$requirements->mysqli = true;

// Check for PDO support ?
$requirements->pdo = true;

// Check for sockets support ?
$requirements->sockets = true;
```

### Requirements
The only requirement for this script is PHP >= 4.3