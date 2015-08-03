# Elixir Sips Ep. 5 - Modules and Mix


## Starting a new project with mix

```bash
mix new my_project
```


## Defining modules and functions

```elixir
defmodule MyModule do
  def my_function(params) do
    params
  end
end
```


## writing documentation

```elixir

# mix.exs
...
defp deps do
  [
    {:ex_doc, "~> 0.7.3"},
    {:earmark, ">= 0.0.0"}
  ]
end
...

# documenting
defmodule ModulesExample do
  @moduledoc """
    A module used for training in [ElixirSips](http://www.elixirsips.com).
  """

  @doc """
    Returns the message it is provided.
  """
  def publish(message) do
    message
  end
end
```


## building and viewing documentation

Use the `h()` function inside of iex or ...

``` bash
mix deps.get
mix docs
open doc/index.html
```
