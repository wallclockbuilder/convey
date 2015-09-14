Convey is awesome Go testing
==============================

[![Build Status](https://travis-ci.org/smartystreets/convey.png)](https://travis-ci.org/smartystreets/convey)
[![GoDoc](https://godoc.org/github.com/smartystreets/convey?status.svg)](http://godoc.org/github.com/smartystreets/convey)

Installation
------------

	$ go get github.com/smartystreets/convey

[Quick start]
-----------

Make a test, for example:

```go
func TestSpec(t *testing.T) {

	// Only pass t into top-level Convey calls
	Convey("Given some integer with a starting value", t, func() {
		x := 1

		Convey("When the integer is incremented", func() {
			x++

			Convey("The value should be greater by one", func() {
				So(x, ShouldEqual, 2)
			})
		})
	})
}
```

Just do what you do best:

    $ go test

Or if you want the output to include the story:

    $ go test -v
