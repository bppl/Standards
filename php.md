## PHP

### PHP Syntax

* Use one space after and before `=`.
* Use one space after and before `{` and `}`
* Use one space after `(` and before `)`
* Use soft-tabs with 4 spaces
* Use `list() = array()` when declaring multiple variables.
* Group code by blocks.
* Files should be named as `my-file-name` instead of `my_file_name` or `MyFileName`.


### Brackets

Don't use curly brackets in loops, or if statements that only contain one line

```php
<?php

// If
if ( $validation )
	$text = 'Validation succeed.';

// Foreach
foreach ( $messages as $message )
	echo $message->title;

```

### Declaration

Use `list() = array()` when declaring multiple variables followed by each other.

```php
<?php

// Bad example
$collection = array();
$titles = array();
$time = time();

// Good example
list( $collection, $titles, $time ) = array( array(), array(), time() );

```

When declaring multiple variable with the same value, assign them all at one.

```php
<?php

// Bad example
$collection = array();
$posts = array();
$news = array();

// Bad example
list( $collection, $posts, $news ) = array( array(), array(), array() );

// Good example
$collection = $posts = $news = array();

```


### Function documentation

When create a function, write a little commentary about what it does, then an example and the the parameters it receive and what it returns.

```php
<?php

/**
* Dumps in a pretty format the passed variable.
*
* <code>
*
*     // Dump a variable
*     dump( $my_var );
*
* </code>
*
* @param { mixed } variable to dump
* @return { void }
*/
function dump( $thing ) {
 
    echo '<pre>';
        var_dump( $thing );
    echo '</pre>';
}
```
