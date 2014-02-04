## PHP Styleguide
Towards a more readable and maintainable code.

## Table of contents

1. [General](#general)
2. [Brackets](#brackets)
3. [Variables](#variables)
4. [Functions](#functions)
 

-------

### General

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

### Variables

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


### Functions

**Documentation**

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

**Return values**

When posible, return directly a comparison of the variable.

```php
<?php

// Good example
function my_function( $a, $b ) {
	
	// Directly return the result of the comparison
	return $a < $b;
}

// Bad example
function my_function( $a, $b ) {

	if ( $a < $b )
		return true;
	else 
		return false;

}

```

When posible, return functions that return a boolean, instead of making an if statement.

```php
<?php

function has_item( $item, $array ) {
	
	// Directly return the result of the comparison
	return in_array( $item, $array );
}



Also, when direct comparison cannot be returned, return on the first if and then keep as normal

```php
<?php

// Good example
function my_function( $a, $b ) {
	
	if ( $a < $b )
		return 1;
		
	return $a * 2;

}

// Bad example
function my_function( $a, $b ) {
	
	if ( $a < $b )
		return 1;
		
	else 
		return  $a * 2;

}
```

**Short if statements**

Use short if statements when appropriate

```php
<?php

// Good example
function my_function( $a, $b ) {

	return $a == 1 ? 'One' : 'Not one';
}

// Bad example
function my_function( $a, $b ) {
	
	if ( $a == 1 )
		return 'One';
		
	else
		return 'Not one';
}

```
