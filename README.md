hashargs.js
===========

A decorator utility to allow any Node.js function to be calls with a hash of named arguments.

Usage
=====

```
> hashify = require('hashargs');
[Function]
> function test(foo, bar, baz, blah) { console.log(arguments); }
undefined
> var t = hashify(test);
undefined
> t({bar: 'hello world'})
{ '0': undefined,
'1': 'hello world',
'2': undefined,
'3': undefined }
undefined
> t({bar: 'hello world'}, blah: 1234)
...
> t({bar: 'hello world', blah: 1234})
{ '0': undefined, '1': 'hello world', '2': undefined, '3': 1234 }
undefined
>
```
