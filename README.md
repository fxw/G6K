# G6K

G6K is a tool that enables the creation and online publishing of calculation simulators without coding. It has a simulation engine and an administration module.

A calculation simulator is an online service made available to a user to enable them to calculate the results (taxes, social benefits, etc.) corresponding to their particular situation. The results are calculated on the basis of data supplied by the user, reference data (eg amount of a tax) and business rules reflecting the current legislation in the field of simulation.

[Learn more](http://eureka2.github.io/g6k/documentation/en/learn-more.html)

## Prerequisites for Symfony 2
* PHP Version 5.3.3 + (recommended 5.5.9+)
* JSON enabled
* ctype
* date.timezone in php.ini
* auto_detect_line_endings = On in php.ini
* PHP-XML module 
* 2.6.21+ version of libxml
* PHP tokenizer 
* Modules mbstring, iconv, POSIX (only on * nix), Intl with ICU 4+, and APCU 3.0.17+ APC (highly recommended) must be installed
* recommended php.ini settings:
  * short_open_tag = Off
  * magic_quotes_gpc = Off
  * register_globals = Off
  * session.auto_start = Off

## Prerequisites for G6K
* PDO enabled
* pdo_pgsql and / or pdo_sqlite activated
* pgsql and / or sqlite3 activated
* SimpleXML enabled
* serialize_precision = -1

## Installation
1. If you plan to use MySQL or PostgreSQL, create a user with "CREATE DATABASE" and "CREATE TABLE" privileges using the administration tool of your RDBMS.
2. Be placed in the <DOCUMENT_ROOT> Web Server
3. Download composer.phar (https://getcomposer.org/download/) in <DOCUMENT_ROOT>
4. Under a shell or DOS, execute: ``php -d memory_limit=-1 composer.phar create-project eureka2/g6k simulator/`` 
5. Enter the parameter values required by the installer, including:
  * database_driver => pdo_pgsl, pdo_mysql or pdo_sqlite
  * database_host => name or IP address of your database server (simply &lt;Enter&gt; in case of SQLite)
  * database_port => port of the database server (simply &lt;Enter&gt; in case of SQLite)
  * database_name => name of the database where the users of the administration interface will be installed 1. (simply &lt;Enter&gt; in case of SQLite)
  * database_user => User name for connecting to the database (simply &lt;Enter&gt; in case of SQLite)
  * database_password => this user's password (simply &lt;Enter&gt; in case of SQLite)
  * database_path => used in the case of SQLite and ignored in other cases, so make &lt;Enter&gt;
  * locale => en 

Normally the installer displays the message 'Installing the users of the administration interface'  
However, on some platforms, this message does not appear. If so, run the following commands:  
``cd simulator``  
``php ../composer.phar run-script post-install-cmd``

## Documentation

### Administrator's Guide

[ [en](http://eureka2.github.io/g6k/documentation/en/index.html) ] 
[ [fr](http://eureka2.github.io/g6k/documentation/fr/index.html) ] 

### Classes

[Documentation of G6K classes](http://eureka2.github.io/g6k/documentation/classes/)

## Innovation Award

<table class="framed light" border>
  <tr>
    <td>
      <a href="https://www.phpclasses.org/" title="PHP Classes" alt="PHP Classes">
        <img src="https://files.phpclasses.org/graphics/phpclasses/logo-small-phpclasses.svg" width="75" height="24" alt="PHP Classes" style="vertical-align: top">
      </a>
     </td>
    <td>
     <b><a href="https://www.phpclasses.org/package/10556-PHP-Generate-simulator-tools-to-perform-calculations.html">G6K</a>
       By <a href="https://www.phpclasses.org/browse/author/549500.html">eureka2</a></b>
     </td>
    <td>
      <a href="https://www.phpclasses.org/award/innovation/"><img src="https://www.phpclasses.org/award/innovation/nominee.gif" width="89" height="89" alt="PHP Programming Innovation award nominee" title="PHP Programming Innovation award nominee" border="0"></a><br><b><span style="font-size: large">April 2018 Number 6</span></b>
    </td>
  </tr>
  <tr>
    <td colspan="3">
      There are many sites that are useful because they provide means to let the users perform calculations of some kind from simple values entered in Web forms.
      <br>
      This package provides a Web interface to implement a generic system for designing and providing access to pages that provide several types of calculator tools.
      <br>
      Manuel Lemos
	</td>
  </tr>
</table>

## Copyright and license

&copy; 2015-2018 Eureka2 - Jacques Archimède. Code released under the [MIT license](https://github.com/eureka2/G6K/blob/master/LICENSE).

