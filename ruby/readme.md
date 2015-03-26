## Ruby Cheat Sheet

### Contents
- [Variables](#variables)
- [Arrays](#arrays)
- [Hashes](#hashes)
- [Strings](#strings)
- [Functions](#functions)
- [Classes](#classes)
- [Debugging](#debugging)

### Variables
Declare a variable
```ruby
foo = "bar"
```
```irb
> foo
=> "bar"
```

### Arrays
<a href="http://ruby-doc.org/core-2.2.0/Array.html" target="_blank">Documentation</a>

Declare an empty array
```ruby
arr = []
```

Declare an array with contents
```ruby
numbers = [1,2,3,4,5]
```

Length of an array
```irb
# For arrays, either .count() and .length() can be used
> [].count
=> 0

> [].length
=> 0

> numbers.length
=> 5
```

Ugly print an array (each element on a new line)
```irb
> puts numbers
1
2
3
4
5
=> nil
```

Pretty-print an array
```irb
> puts numbers.to_s
[1, 2, 3, 4, 5]
=> nil
```

### Hashes
<a href="http://ruby-doc.org/core-2.2.0/Hash.html" target="_blank">Documentation</a>

Declare an empty hash
```ruby
h = {}
```

Declare a hash with contents
```ruby
h = { "a" => "alpha", "b" => "bravo", "c" => "charlie" }
```

Get a value from a hash
```irb
> h["a"]
=> "alpha"
```

Add to a hash
```ruby
> h["d"] = "delta"
=> "delta"
> h
=> {"a"=>"alpha", "b"=>"bravo", "c"=>"charlie", "d"=>"delta"}
```

### Strings
<a href="http://ruby-doc.org/core-2.2.0/String.html" target="_blank">Documentation</a>

Get the length of a string
```ruby
> s = "hello"

> "hello".length
=> 5

> s.length
=> 5
```

Reference characters of a string by index
```ruby
> s = "hello"

> "hello"[0]
=> "h"

> s[0]
=> "h"
```

### Functions
Function with no arguments
```ruby
def say_hello
  puts "Hello."
end

> say_hello
Hello.
=> nil
```

Function with arguments
```ruby
def say_hello(name)
  puts "Hello, #{name}."
end
```

```irb
> say_hello("campo")
Hello, campo.
=> nil
```

Function with default argument value
```ruby
def say_hello(name="person")
  puts "Hello, #{name}."
end
```

```irb
> say_hello
Hello, person.
=> nil

> say_hello("campo")
Hello, campo.
=> nil
```

### Classes
Declare a class
```ruby
class ClassName < ParentClass
  @@class_variable = 0 # Visible to all instances of this class

  def initialize
    # class initialize method
    @instance_variable = 0 # Visible only to this instance
  end

  def instance_method
    puts "This takes no arguments."
  end
end
```

### Debugging
Raise a runtime exception (execution stops) that prints out the contents of the object foo
```ruby
raise foo.inspect
```
