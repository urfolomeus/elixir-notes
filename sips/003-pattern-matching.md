# Elixir Sips Ep. 3 - Pattern Matching

## = is the match operator, not assignment

`foo = 1  => 1`

`foo      => 1`

`1 = foo  => 1`


## pattern matching examples

`{:foo, bar} = {:foo, 3}  => {:foo, 3}`

`bar                      => 3`

### Use `_` to ignore a value

`{_, baz} = {1, 2}        => {1, 2}`

`baz                      => 2`

### Use `^` to instruct Elixir not to rebind a variable

`[a, 2] = [1, 2]   => [1, 2]`

`a                 => 1`

`[a, 2] = [3, 2]   => [3, 2]`

`a                 => 3`

`[^a, 2] = [4, 2]  => ** (MatchError)`
