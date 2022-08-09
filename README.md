# Please no more setters/getters with no reasons.

### Readonly, immutable object

```php
class Input
{
  public function __construct(private ?string $value = null): self
  {
  }
  
  public function getValue(): ?string
  {
    return $this->value;
  }
}
```

### Type casting 

```php
class Input
{
  private const PREFIX = 'xxx';
  
  private mixed $value = null;

  // Type casting
  public function printValue(): string
  {
    return self::PREFIX . (string)$this->value;
  }

}
```

### Object is available for modification(mutable)
```php
class Input
{
  public ?string $value = null;
}
```
