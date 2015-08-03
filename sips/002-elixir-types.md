# Elixir Sips Ep. 2 - Elixir Types

## Numbers

`1 + 2      => 3`

`1 - 2      => 1`

`1 * 2      => 2`

`1 / 2      => 0.5`

`div(1, 2)  => 0`

`rem(1, 2)  => 1`


## Collections

`[1, 2, 3]                                        # list`

`{:foo, :bar, :baz}                               # tuple`

`[author: "Josh Adams", title: "Basic Elixir"]    # keyword list`


## Regex

Uses Perl-compatible regex.

`Regex.replace ~r/[aeiou]/, "Beginning Elixir", "z"  => "Bzgznnzng Elzxzr"`


## Boolean

Everything apart from `false` and `nil` are truthy.

`true == :true  => true`

`false == :false  => true`

`nil == :nil  => true`
