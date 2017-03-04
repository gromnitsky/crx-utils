# crx-utils

## zip2crx

~~~
$ openssl genrsa 1024 > private.pem
$ ./zip2crx foo.zip private.pem
~~~

## crx2zip

Extracts a public key, a signature & a .zip archive.

~~~
$ ./crx2zip foo.crx alice.pub
  RSA key                 1024 bits
  Total header size:      306 bytes
  Public key:             foo/key.der
  Signature status:       Verified OK
~~~

Optionally checks the .crx w/ another public key in the DER format:

~~~
$ ./crx2zip foo.crx alice.pub
  RSA key                 1024 bits
  Total header size:      306 bytes
  Public key:             alice.pub
  Signature status:       Verification Failure
~~~

## TODO

- check in each script for required utils
- add an example for Make

## License

MIT.
