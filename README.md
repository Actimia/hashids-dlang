#D Hashids
A [D](http://dlang.org/) port of [hashids](http://hashids.org/), a library for encoding integer sequences as opaque, url-friendly blobs.
##Usage
```d
import hashids;
auto hasher = new Hashids();
string hash = hasher.hash(1, 2, 3); // "o2fXhv"
ulong[] numbers = hasher.decode(hash); // [1, 2, 3]
```
Hashid constructor takes three optional parameters:
 - salt (a string)
 - minimum hash length (a uint)
 - alphabet (a string)

##Installation
```json
"dependencies": {
    "hashids": ">=1.0.0"
}
```

##Acknowledgements
 - [python-hashids](https://github.com/davidaurelio/hashids-python) for excellent unittests which were ported over.
