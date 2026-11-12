# base-unit-trait-ignores-fortifications

The `IgnoresFortifications` unit trait: a unit type with it ignores fortifications when it attacks.

A unit type with this trait gets no penalty from a defender's city walls or fortress.

For example: Civ1: Artillery and Bomber. Civ2: flag 6 (Howitzer).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(IgnoresFortifications)`:

```ts
import IgnoresFortifications from '@civ-clone/base-unit-trait-ignores-fortifications/IgnoresFortifications';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, IgnoresFortifications));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
