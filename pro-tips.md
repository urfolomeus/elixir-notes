# Pro-tips

These are various tidbits found that might come in useful at some point. :)

## storing history between IEx sessions

1. `git clone git@github.com:ferd/erlang-history.git`
2. `cd erlang-history`
3. `sudo make install`

## pattern matching for strings that start with a given value

```elixir
def my_func("prefix" <> rest = value) do
  IO.puts "#{value} starts with \"prefix\""
end
```

## maintaining state in Erlang

From the Elixir slack:

> Hey guys :simple_smile: I'm learning how you're supposed to keep state in processes by recursion. But I was wondering...doesn't this eventually end in a stack too deep? If the process keeps spawning itself after receiving and handling a message, with the new state, can it keep doing that infinitely? How?

> gerred [5:45 AM]
> @xtagon look up tail call optimization, the BEAM VM does it. :simple_smile:

> cpjk [5:54 AM]
> Along with what @gerred said, OTP also provides nice behaviours for spawning processes to maintain state, so that you don't have to think about it. This [SO answer](http://stackoverflow.com/questions/26713811/how-to-maintain-state-in-erlang/26714738#26714738) might help.


## getting the AST of some code

`quote` returns the AST of some code

```elixir
iex(1)> quote do
...(1)> 1 + 2
...(1)> end
{:+, [context: Elixir, import: Kernel], [1, 2]}
```

## Module definitions contain a binary of their definition

If you capture the output of a defined module you can see that the third item is a binary representation of the module which apparently means that you can pass the definition around from node to node and have it execute even though there is no local version of the definition.

```elixir
iex(1)> my_module = defmodule MyModule do
...(1)>   def test(message) do
...(1)>     message
...(1)>   end
...(1)> end
{:module, MyModule,
 <<70, 79, 82, 49, 0, 0, 4, 148, 66, 69, 65, 77, 69, 120, 68, 99, 0, 0, 0, 117, 131, 104, 2, 100, 0, 14, 101, 108, 105, 120, 105, 114, 95, 100, 111, 99, 115, 95, 118, 49, 108, 0, 0, 0, 2, 104, 2, ...>>,
 {:test, 1}}
```

## Loading config files

> Paul Wilson [10:51 AM]
> \#til You can load extra Mix config files using. This is useful for excluding secret stuff from source control.

`import_config “extraconfigfile.exs"`
