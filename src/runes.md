
Runes 符文概念是 Svelte 语言语法的一部分, 类似语言关键字.

Runes look like functions, but they’re not — when you use Svelte, they’re part of the language itself

### $state: allows you to create reactive state

Unlike other frameworks you may have encountered, there is no API for interacting with state — count is just a number, rather than an object or a function, and you can update it like you would update any other variable.

#### deep state 

Proxy 代理实现(Javascript 的基本能力)

结构的对象属性会失去 reactive

如果不想使用 deep state, 可以用 $state.raw 来声明;

在函数中使用 $state

### $drived

```svelte
let count = $state(0);
let double = $derived(count * 2);
```

复杂的依赖逻辑可以使用 $derived.by
Unlike normal state, derived state is read-only.

本质上, $derived(expression) 等同于 $derived.by(() => expression).

实现逻辑: 

Anything read synchronously inside the $derived expression (or $derived.by function body) is considered a dependency of the derived state. When the state changes, the derived will be marked as dirty and recalculated when it is next read.

untrack 可以实现取消依赖标记.
- https://svelte.dev/docs/svelte/svelte#untrack

Svelte 使用推拉式的更新机制, 状态更新时会导致所有依赖项收到推送而改变, 但是 derived 是真正读取时才重新计算, 而且还会判断是否与前值相同来跳过下游更新;

### $effect

run code before the DOM update: $effect.pre





