# Elixir Sips Ep. 4 - Functions

## Anonymous functions

```elixir
print_name = fn
  { :person, first_name, last_name } -> "#{first_name} #{last_name}"
end

print_name.({ :person, "Alan", "Gardner" })   => "Alan Gardner"
```

```elixir
# calling an anonymous function immediately
(fn -> "foo" end).()   => "foo"
```

## functions are first class citizens

### currying

```elixir
add = fn
  num -> (fn num2 -> num + num2 end)
end
=> #Function<blah>
add3 = add.(3)
=> #Function<blah>
add3.(5)
=> 8
```

### higher order functions

```elixir

```
