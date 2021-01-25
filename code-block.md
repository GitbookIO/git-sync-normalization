# Code block

### Example without tabs

```ruby
def greeting(name)
  puts "Hello #{name}"
end
greeting("Anna")
```

### Example with tabs

{% tabs %}
{% tab title="Ruby" %}
```ruby
def greeting(name)
  puts "Hello #{name}"
end
greeting("Anna")
```
{% endtab %}

{% tab title="Elixir" %}
```elixir
greeting = fn (name) -> "Hello, #{name}!" end
greeting.("Anna")
```
{% endtab %}
{% endtabs %}



