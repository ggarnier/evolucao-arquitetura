## Cache

- 2 níveis (performance e stale)
- diferentes tempos para cada serviço

https://github.com/globocom/content-gateway-ruby

```ruby
menu_config = OpenStruct.new(
  cache: Rails.cache,
  timeout: 1,
  cache_expires_in: 30.minutes,
  cache_stale_expires_in: 2.days
)

gateway = ContentGateway::Gateway.new("Menu", menu_config, UrlGenerator.new)

gateway.get_json("/api/menu.json")
```
