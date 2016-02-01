PHP-FIG 发布代码的命名约定
===============================================

1. 接口必须以 `Interface` 为后缀：例如，`Psr\Foo\BarInterface`。
2. 抽象类必须以 `Abstract` 为前缀：例如，`Psr\Foo\AbstractBar`。
3. Traits 必须以 `Trait` 为后缀：例如，`Psr\Foo\BarTrait`。
4. 必须遵循 PSR-1，2 和 4。
5. 包命名空间必须是 `Psr`。
6. 必须有和 PSR 有关的<包名/二级>命名空间覆盖代码。
7. Composer 包必须命名为 `psr/<package>`，例如，`psr/log`。如果包需要一个虚拟的实现，则实现必须命名为 
`psr/<package>-implementation` 并且以特定的版本被引入，例如 `1.0.0`。然后 PSR 
的实现者可以在他们的包中提供 `"psr/<package>-implementation": "1.0.0"` 去满足需求。未来 PSR 
的规格更改只能通过给 `psr/<package>` 包打新的 tag 完成，并且需求一个同样版本的实现。