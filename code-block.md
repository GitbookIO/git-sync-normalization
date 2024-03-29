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

### Example with filename

{% code title="greeting.rb" %}
```ruby
def greeting(name)
  puts "Hello #{name}"
end
greeting("Anna")
```
{% endcode %}

### JavaScript example

{% code title="index.js" overflow="wrap" lineNumbers="true" %}
```javascript
‌import * as React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(<App />, window.document.getElementById('root'));
```
{% endcode %}
