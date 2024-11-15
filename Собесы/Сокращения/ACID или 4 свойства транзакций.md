**Atomicity** (атомарность) — выражается в том, что транзакция должна быть выполнена в целом или не выполнена вовсе.

**Consistency** (согласованность) — гарантирует, что по мере выполнения транзакций, данные переходят из одного согласованного состояния в другое, то есть транзакция не может разрушить взаимной согласованности данных.

Например, в банковской системе может существовать требование равенства суммы, списываемой с одного счёта, сумме, зачисляемой на другой. Это бизнес-правило и оно не может быть гарантировано только проверками целостности базы данных. Это поведение должны учитывать программисты при написании кода транзакций. Если какая-либо транзакция произведёт списание, но не произведёт зачисления, то система останется в некорректном состоянии и свойство согласованности будет нарушено.

**Isolation** (изолированность) — Во время выполнения транзакции параллельные транзакции не должны оказывать влияние на её результат.

Изолированность обходится дорого, поэтому в реальных базах данных существуют режимы, не полностью изолирующие транзакцию. Об уровнях изоляции мы поговорим в отдельной статье.

**Durability** (долговечность) — Независимо от проблем с оборудованием, изменения, сделанные успешно завершённой транзакцией, должны остаться сохранёнными после возвращения системы в работу.