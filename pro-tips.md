# Pro-tips

These are various tidbits found that might come in useful at some point. :)

## pattern matching for strings that start with a given value

```
def my_func("prefix" <> rest = value) do
  IO.puts "#{value} starts with \"prefix\""
end
```
