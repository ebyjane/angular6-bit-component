# angular6-for-bit-component
Angular6 with shared components

Below Components are created using Angular6 and pushed to bit 

You can find the same in below URL

https://bitsrc.io/ebyjane/angular/global/ui

Details of the same is mentioned below.

diff (firstArray:[], secondArray:[]) : []

Computes the difference between two array references.
Example

diff([1,2,3], [1,2,3,4,5]) // => [4,5]

Arguments
firstArray
:
[]

secondArray
:
[]

Returns
[]

returns an array representing the difference between the two arrays
first (array:[]) : (* | null)

Returns the first element of an array.
Example

first([1, 2, 3]) // => 1
  first(['a', 'b', 'c']) // => 'a'

Argument
array
:
[]

Returns
(* | null)

first element of given array
flatMap (array:[*], cb:Function) : [*]

Builds a new collection by applying a function to all elements of this array and using the elements of the resulting collections.
Example

flatMap([[1, 2, 3], [4, 5, 6]], val => val) // => [1, 2, 3, 4, 5, 6]

Arguments
array
:
[*]

cb
:
Function

Returns
[*]

makeArray (val:*) : [*]

Wraps a value with an array.
Example

makeArray(1) // => [1]
 makeArray([1]) // => [1]
 makeArray(null) // => []

Argument
val
:
*

Returns
[*]

an ssh client for consuming bit components from a remote scope

A ponyfill for Buffer.from, uses native implementation if available.
sha1 (:(string | Buffer), encoding:string) : string

encrypt data buffer or string into a sha1 hash
Example

sha1('foo bar') // => '3773dea65156909838fa6c22825cafe090ff8030'

Arguments
(string | Buffer)

encoding
:
string

Returns
string

sha1 hash
extractFileNameFromPath (filePath:string) : string

Recieves a file path and returns the file name
Argument
filePath
:
string

Returns
string

compose (functions:Array<function>) : function

compose functions into one function from right to left
Argument
functions
:
Array<function>

Returns
function

pipe (functions:Array<function>) : function

compose functions from left to right
Example

pipe(func1, func2, func3)(val) === func3(func2(func3(val)))

Argument
functions
:
Array<function>

Returns
function

toKubeformat (bitId:String) 

Convert bit id to acceptable kubernetes job name
Argument
bitId
:
String

Returns

String
clamp (value:number, min:number, max:number) : number

Returns a number whose value is limited to the given range.
Example

clamp(50, 5, 10) // => 5

Arguments
value
:
number

The value to be clamped
min
:
number

The lower boundary of the output range
max
:
number

The upper boundary of the output range
Returns
number

A number in the range [min, max]
clean (obj:object) : object

Cleans all object’s properties that contains a falsy value and returns a new object without them.
Example

new cleaned object
 clean({ foo: null, bar: 'foo' }) // => { bar: 'foo' }

Argument
obj
:
object

object to clean
Returns
object

evolve (transformations:Object, object:Object) : Object

Creates a new object by recursively evolving a shallow copy of object, according to the transformation functions. All non-primitive properties are copied by reference.

A transformation function will not be invoked if its corresponding key does not exist in the evolved object.
Example

var tomato  = {firstName: '  Tomato ', data: {elapsed: 100, remaining: 1400}, id:123};
     var transformations = {
       firstName: trim,
       lastName: trim, // Will not get invoked.
       data: {elapsed: add(1), remaining: add(-1)}
     };
     evolve(transformations, tomato); //=> {firstName: 'Tomato', data: {elapsed: 101, remaining: 1399}, id:123}

Arguments
transformations
:
Object

The object specifying transformation functions to apply to the object.
object
:
Object

The object to be transformed.
Returns
Object

The transformed object.
forEach (obj:object, cb:function) 

Invoke a function for every key within given object or array.
Example

forEach({ a: 1, b: 2, c: 3 }, (val, key) => console.log(key, val));
 // => a 1 b 2 c 3

Arguments
obj
:
object

object or array to iterate
cb
:
function

callback function to invoke
groupBy (collection:(Array | Object), iteratee:Function) : Object

Creates an object composed of keys generated from the results of running each element of collection thru iteratee. The order of grouped values is determined by the order they occur in collection. The corresponding value of each key is an array of elements responsible for generating the key. The iteratee is invoked with one argument: (value).
Example

groupBy([6.1, 4.2, 6.3], Math.floor)
// => { '4': [4.2], '6': [6.1, 6.3] }

Arguments
collection
:
(Array | Object)

The collection to iterate over.
iteratee
:
Function

The iteratee to transform keys.
Returns
Object

Returns the composed aggregate object.
hasOwnProperty (obj:object, prop:(string | number)) : boolean

Determines whether the object has the specified property.
Example

hasOwnProperty({foo: 'bar'}, 'foo') // => true
 hasOwnProperty({foo: 'bar'}, 'bar') // => false

Arguments
obj
:
object

prop
:
(string | number)

property to test
Returns
boolean

map (object:object, iteratee:function (val, key)) : object

Returns the results of applying the iteratee to each element of the object.
Example

const newObj = mapObject({ start: 5, end: 12 }, function(val, key) {
  return val + 5;
});
console.log(newObj) //  { start: 10, end: 17 }

Arguments
object
:
object

iteratee
:
function (val, key)

Returns
object

mergeAll (:array<object>) : object

merge an array of objects
Argument
array<object>

Returns
object

merge () 

Merges multiple objects into one
Example

const o1 = { a: 1 };
const o2 = { b: 2 };
const o3 = { c: 3 };

const obj = merge(o1, o2, o3);
console.log(obj); // { a: 1, b: 2, c: 3 }
console.log(o1);  // { a: 1 } does not mutate objects

values (object:object) : []

get all object values.
Example

values({ a: 1, b: 2, c: 3 }) // => [1, 2, 3]

Argument
object
:
object

Returns
[]

object's values
getData (cache:RedisClient, key:string, fields:(string | Array.<string>)) : Promise<Array.<string>>

Returns a Promise resolved with the values associated with the specified fields in the hash stored at key.
Arguments
cache
:
RedisClient

-
key
:
string

hash stored at key
fields
:
(string | Array.<string>)

Returns
Promise<Array.<string>>

list of values associated with the given fields, in the same order as they are requested.
setData (cache:RedisClient, key:string, fields:(string | Array.<string>)) : Promise<Array.<string>>

Returns a Promise resolved with the values associated with the specified fields in the hash stored at key.
Arguments
cache
:
RedisClient

-
key
:
string

hash stored at key
fields
:
(string | Array.<string>)

Returns
Promise<Array.<string>>

list of values associated with the given fields, in the same order as they are requested.
parseUrl (url:string) : object
Argument
url
:
string

Returns
object

{ host, path, port, username }
cleanChar (str:string, char:string) : string

cleans the first occurence of char from str reference.
Example

cleanChar('hello', 'h') // => 'ello'

Arguments
str
:
string

string to perform cleaning on.
char
:
string

character to clean from string
Returns
string

cleaned string.
contains (str:string, searchStr:string) : boolean

determines whether string str ref contains substring searchRef.
Example

contains('foo bar', 'bar') // => true
 contains('foo', 'bar') // => false

Arguments
str
:
string

searchStr
:
string

Returns
boolean

fromBase64 (base64:string) : string

decode a string from base64
Argument
base64
:
string

Returns
string

leftPad (str:string, len:number, ch:string) : string

pad a string to the left.
Example

leftPad('foo', 5) // => "  foo"
 leftPad('foobar', 6) // => "foobar"
 leftPad(1, 2, '0') // => "01"

Arguments
str
:
string

string to pad
len
:
number

total
ch
:
string

char to use for padding
Returns
string

modified string
removeNewLines (str:string) : string

remove all new lines from a string (do not mutate the string but return new instance)
Argument
str
:
string

Returns
string

startsWithOneOf (str:string, options:Array) : bool

Checks whether the string start with on the options specified.
Example

startsWithOneOf('hello', ['h', 'afdsf']) // => true
startsWithOneOf('hello', ['g', 'afdsf']) // => false

Arguments
str
:
string

string to check.
options
:
Array

options to start with
Returns
bool

whether the string starts with one of the options.
toBase64 (val:(string | Buffer)) : string

encode a string or a buffer to base64
Example

toBase64('foo bar') // => Zm9vIGJhcg==
 toBase64(new Buffer('foo bar')) // => Zm9vIGJhcg==

Argument
val
:
(string | Buffer)

string or buffer to encode
Returns
string

base64 encoded string
empty (name:*) : boolean

determines whether obj reference is empty (empty array, empty object and/or falsy values)
Example

empty([]) // => true
 empty({}) // => true
 empty(1) // => false
 empty('') // => false
 empty('foo') // => false
 empty(false) // => true

Argument
name
:
*

Returns
boolean

isEmail (email:string) : boolean

simple email validator
Example

isEmail('not an email') => false
isEmail('valid.email@gmail.com') => true
isEmail('@invalid.com') => false

Argument
email
:
string

the email to validate upon
Returns
boolean

isNil (val:*) : boolean

determines whether val reference is null or undefined.
Example

isNil(null) // => true
 isNil('') // => true

Argument
val
:
*

Returns
boolean

isNumber (val:*) : boolean

determiens whether val is a number.
Example

isNumber('') // => false
isNumber(54) // => true
isNumber('number') // => false
isNumber(64.236) // => true

Argument
val
:
*

Returns
boolean

isString (val:*) : boolean

detemines whether str is a string.
Example

isString(3) // => false
 isString('') // => true

Argument
val
:
*

Returns
boolean
