# m.attrs.bidi
Bi-directional binding for Mithril!

As a custom attribute (requires [custom attribute fork](#m.attrs)):

```javascript
m( 'input', {
	bidi : valueProp
} )
```

[Custom attribute demo](http://jsfiddle.net/barney/9dshk29d/).

...Or as a component (ensures lexical reference):

```javascript
bidi( {}, m( 'input' ), valueProp )
```

[Component demo](http://jsfiddle.net/barney/4tb25zwg/)

### Gimme!

```shell
# NPM
npm install m.attrs.bidi --save

# Bower
bower install m.attrs.bidi --save
```

When

```javascript
// Node / Browserify
var bidi = require( 'm.attrs.bidi' )

// ES6
import bidi from 'm.attrs.bidi'

// RequireJS
require( [ 'm.attrs.bidi' ], function( bidi ){
	/* ... */
} )

// HTML
<script src="https://cdn.rawgit.com/barneycarroll/m.attrs.bidi/master/bidi.js"></script>
<script>
 window.bidi = m.attrs.bidi;
</script>
```

### How

#### Dropdowns

Dropdowns will need their options passed in as normal.

```javascript
m( 'select', {
	bidi : valueProp
},
	list.map( function( item ){
		return m( 'option', item )
	} )
)
```

#### Radio buttons

In the same way, radio buttons need to have values specified

```javascript
m( 'input[type=radio]', {
	bidi  : valueProp,
	value : item1
} ),
m( 'input[type=radio]', {
	bidi  : valueProp,
	value : item2
} )
```

#### Checkboxes

```javascript
m( 'input[type=checkbox]', {
	bidi : valueProp
} )
```
