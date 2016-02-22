# motranslator

PHP Gettext mo files translator

## Performance

This library was tweaked for best performance for single use - translating
application with many strings using mo file.

Current benchmarks show it's about four times faster than original php-gettext.

The performance improvements based on individual changes in the code:

| Stage          | Seconds         |
| -------------- | --------------- |
| Original code  | 4.7929680347443 |
| Remove nocache | 4.6308250427246 |
| Direct endian  | 4.5883052349091 |
| Remove attribs | 4.5297479629517 |
| String reader  | 1.8148958683014 |
| No offset      | 1.2436759471893 |
| Less attribs   | 1.1722540855408 |
