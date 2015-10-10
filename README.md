#D Hashids
A [D](http://dlang.org/) port of [hashids](http://hashids.org/), a library for encoding integer sequences as opaque, url-friendly blobs. All feedback/pull requests are welcome.
###Usage
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

###Installation
Either fork/clone this Github project, or add this project as a DUB dependency like this:
```json
"dependencies": {
    "hashids": ">=1.0.0"
}
```

###Contact
Either through Github issues/PRs or [@actim1a](https://twitter.com/Actim1a) on Twitter.

###Acknowledgements
 - [python-hashids](https://github.com/davidaurelio/hashids-python) for excellent unittests which were ported over.
