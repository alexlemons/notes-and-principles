# Data Types

### Numeric

Signed numbers use 1-bit for +/- sign

`Integer, 8-bit, signed:` -128 to +127

`Integer, 8-bit, unsigned:` 0 to +255

`Integer, 16-bit, signed:` -32768 to +32767

`Integer, 16-bit, unsigned:` 0 to +65535

`Integer, 32-bit, signed:` -2147483648 to +2147483647

`Float, 32-bit:` -3.4028237 to +3.4028237 x 10³⁸ (7 decimal digits of precision)

`Higher precision float formats`: 64-bit Double, 128-bit Quadruple, 256-bit Octuple.

### Array Buffer

A data buffer is a block of memory allocated to temporarily store data while it is being moved in and out of a system. Array buffers represent a fixed length byte array, where each index represents one byte aligned in memory.

In JS you cannot manipulate the contents of an ArrayBuffer directly, instead you use a view that sits on top and offers an api to perform read and write operations. The type of view used depends on your requirements. For example, for `Int8Array/Uint8Array` each index represents one byte and is memory aligned, for `Int32Array/Uint32Array/Float32Array` each index represents four bytes and is memory aligned. Note that their names are misleading, they are not arrays but views referencing an underlying ArrayBuffer.

By informing the system exactly how much space an array buffer will use and how you're going to view it, memory read and write performance can be optimized.
