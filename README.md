
# css `transform` and `transition`

## background/refresher

* css is declarative appearance
* selector and styles

## demo

* cardsmith
* eyescream

## css `transform`

#### [vendor prefixing](http://caniuse.com/#feat=transforms2d)

	```css
	div {
		-webkit-transform: translateY(-1px);
		-moz-transform: translateY(-1px);
		-ms-transform: translateY(-1px);
		-o-transform: translateY(-1px);
		transform: translateY(-1px);
	}
	```
#### value

* Is one _or more_ transformation functions:
	* `translate()`
	* `rotate()`
	* `scale()`
	* more...

* typically: default, X, Y, 3d

* [matrix](http://www.useragentman.com/blog/2011/01/07/css3-matrix-transform-for-the-mathematically-challenged/)

* default 2d functions:
	* `translate(10px, 0)`
	* `rotate(30deg)`
	* `scale(1.25)`

* any web content

### css `transform-origin`

* `transform-origin: x [y] [z]`
* `transform-origin-x: x`
* `transform-origin-y: y`
* `transform-origin-y: z`

values:

* `0`, `50%`, `100%`
* `left`, `right`, `center`, `top`, `bottom`

### gotchas and things to keep in mind

* separate from `top` and `left`**
	* use these for layout
* it is a single style value!
* order matters!
* scale does not compensate for images

### ** modern browsers

Are very optimized for:

* `translate`
* `scale`
* `rotate`
* `opacity`

Use `translate3d(x, y, z)` to engage GPU

### state transitions

simple `:hover` example

## css `transition`

* `transition: property duration easing delay`
* use comma separated list for multiple properties

### property

* `all`

* any numeric based style property

* `transition: all 500ms`

### duration and delay

units `ms` or `s`

### easing

keyword or cubic-bezier ([here](http://cubic-bezier.com/)
or [here](http://matthewlein.com/ceaser/))

### state transitions

* better `:hover` example
* mixed timings
* `:checked` collapse/exand example
* class names

## css `3d`

### css `perspective`

Creates a 3d "space"

```css
perspective: 800;
```

### css `transform-style`

Allows child elements to participate in parent "space"

```css
transform-style: preserve-3d;
```


