There are two different types of numbers in Ruby:

- Integers: numbers with no digits behind the decimal separator (whole numbers). Examples are `-6`, `0`, `1`, `25`, `976` and `500000`.
- Floating-point numbers: numbers with zero or more digits behind the decimal separator. Examples are `-2.4`, `0.1`, `3.14`, `16.984025` and `1024.0`.

They are implemented through the [`Integer`][integer-ruby] and [`Float`][float-ruby] class.
Arithmetic is done using the standard arithmetic operators. Numbers can be compared using the standard numeric comparison operators(`>`, `<=`, `==`, `!=`, etc.).
Basic arithmetic operations between instances of `Integer`, will always result in an instance of `Integer`:

###`+`

```ruby
a = 1 + 2
#=> 3
a.class
#=> Integer
```

###`-`

```ruby
b = 1 - 2
#=> -1
b.class
#=> Integer
```

###`/`

```ruby
c = 1 / 2
#=> 0
c.class
#=> Integer
```

Notice how the division of two instances of `Integer`, resulted in a third instance of `Integer`. Keep it mind that the remainder of a division is discarded. For example: `99/100` is equal to `0`.

###`+`

```ruby
d = 1 * 2
#=> 2
d.class
#=> Integer
```

Basic arithmetic operations between instances of `Float` will result in other instances of `Float`.
Basic arithmetic operations between instances of `Integer` and instances of `Float` will result in instances of `Float`.

```ruby
a = 1
b = 2.0
a.class
#=> Integer
b.class
#=> Float
c = a + b
#=> 3.0 (Notice the decimal separator)
c.class
#=> Float
d = b / 2
#=> 1.0
d.class
#=> Float
```

Both instances of `Float` and `Integer` implement methods to convert values from one to the other. As a number implemented through the `Integer` class has less precision than a number implemented through the `Float` class, converting from an instance of `Integer` to an instance of `Float` is safe because it does not result in any kind of data loss. However, converting from an instance of `Float` to an instance of `Integer` could mean losing data.

In this exercise you must conditionally execute logic. A common way to do this in Ruby is by using an `if/else` statement:

```ruby
x = 5

if x == 5
  # Execute logic if x equals 5
elsif x > 7
  # Execute logic if x greater than 7
else
  # Execute logic in all other cases
end
```

The condition of an `if` statement does not have to be only `true` or `false`. It can be any value. But it's important to know that any value other than `nil` and `false` (_truthy_ values) will be treated as `true`, meaning that the code inside the `if` statement will be executed.

Ruby also implements the `case` statement:

```ruby
y = 5
case y
when 3
  # Execute logic if y equals 3
when 5
  # Execute logic if y equals 5
else
  #Exectue logic in all other cases
end
```

[integer-ruby]: https://ruby-doc.org/core-2.7.1/Integer.html
[float-ruby]: https://ruby-doc.org/core-2.7.1/Float.html
