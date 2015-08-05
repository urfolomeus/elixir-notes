# Pro-tips

These are various tidbits found that might come in useful at some point. :)

## pattern matching for strings that start with a given value

```
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

