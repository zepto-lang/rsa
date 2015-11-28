# rsa

A minimal RSA library in zepto. Port of [the chibi implementation](https://github.com/ashinn/chibi-scheme/blob/23ac772e3ac347d01647952621fbc83b4293448b/lib/chibi/crypto/rsa.scm).

## Usage

There are quite a few functions and a rsa-key record type implemented.
Here are a few example:

```clojure
(load "rsa/rsa")
(define encrypt (import "rsa:encrypt"))
(define decrypt (import "rsa:decrypt"))
(define keygen (import "rsa:keygen"))
(define key (key-gen)) ; will yield a rsa key type with the fields bits (number of bits), n, e and d
; If you don't know what these are, don't bother with them
(define decrypt (encrypt 1000)) ; => 1000
```

Additional methods include `key-gen-from-primes` if you want to supply
your own primes instead of randomly generating them, `pub-key` for getting
the public key part, `sign` for signing a document, `verify` for verifying this
signature and returning the message and `verify?` to test signature and message right away.

<br/>

Have fun!
