# ESLint

Naše defaultní pravidla jsou definována v [`eslint-default.json`](eslint-default.json). Pravidla pro projekt upravuj vždy přímo v daném projektu v souboru `eslint.json`.

Kompletní dokumentace ESLint pravidel zde: https://eslint.org/docs/rules/


## Naše pravidla ve zkratce

### Possible Errors

- **for-direction: error**  
Prevence nekonečných loopů ve `for`.

- **getter-return: error**  
Požaduje `return` v `get` funkcích.

- **no-compare-neg-zero: error**  
Zakázáno porovnání s `-0`.

- **no-cond-assign: error**  
Uvnitř podmínky je zakázáno přiřadit proměnné hodnotu pomocí `=`.

- **no-console: warn**  
Použití `console` hodí varování.

- **no-constant-condition: error**  
V podmínkách je zakázáno použití samotné konstanty, např. `if (false) { ... }`.

- **no-control-regex: error**  
Zákaz neviditelných znaků v regulárních výrazech.

- **no-debugger: error**  
Zákaz použití `debugger`.

- **no-dupe-args: error**  
Ve funkci jsou zakázány stejně pojmenované argumenty.

- **no-dupe-keys: error**  
V objektu jsou zakázány stejně pojmenované vlastnosti.

- **no-duplicate-case: error**  
Ve `switch` jsou zakázány stejně pojmenované `case`.

- **no-empty: error**  
Jsou zakázány prázdné bloky `{ }`.

- **no-empty-character-class: error**  
V regulárních výrazech jsou zakázány prázdné `[]`.

- **no-ex-assign: error**  
V `catch` je zakázáno přepsat hodnotu exception.

- **no-extra-boolean-cast: error**  
V podmínkách je zakázáno zbytečně konvertovat proměnnou na `boolean`.

- **no-extra-semi: error**  
Podchytí středníky navíc.

- **no-func-assign: error**  
Zákaz přepsání funkce jinou proměnnou.

- **no-inner-declarations: error**  
Zákaz deklarace funkce uvnitř vnořených bloků.

- **no-invalid-regexp: error**  
Podchytí nevalidní regulární výrazy.

- **no-irregular-whitespace: error**  
Povoleny pouze obyčejné mezery.

- **no-obj-calls: error**  
Zákaz volání `Math`, `JSON` a `Reflect` jako funkce.

- **no-regex-spaces: error**  
V regulárním výrazu je zakázáno používat několik po sobě jdoucích mezer.

- **no-sparse-arrays: error**  
Žádné pole s prázdnými sloty, např. `[,,]`.

- **no-unexpected-multiline: error**  
Podchytí několikařádkové výrazy, které mají být pravděpodobně pouze na jednom řádku.

- **no-unreachable: error**  
Podchytí kód, který není dosažitelný, např. za `return`.

- **no-unsafe-finally: error**  
Ujištění, že `finally` bude fungovat jak je očekáváno.

- **no-unsafe-negation: error**  
Zákaz negace proměnné před `in` a `instanceof`.

- **use-isnan: error**  
Vynucuje použití `isNaN()` namísto porovnání s `NaN`.

- **valid-typeof: error**  
Podchytí překlepy v typu při porovnávání pomocí `typeof`.


### Best Practices

- **curly: ["error", "all"]**  
Vyžaduje složené závorky `{}` u bloků `if`, `else`, `for` a podobně.

- **dot-notation: warn**  
Varuje při použití hranatých závorek `foo['bar']` místo tečkové konvence `foo.bar`.

- **guard-for-in: error**  
Vyžaduje podmínku `if ({}.hasOwnProperty(...))` ve `for in` loopu.

- **no-alert: warn**  
Varuje při použití `alert`.

- **no-caller: warn**  
Varuje při použití `arguments.caller` a `arguments.callee`.

- **no-empty-function: error**  
Zakazuje prázdné funkce.

- **no-empty-pattern: error**  
Podchytí prázdný "destructuring pattern" při deklaraci proměnné, např. `var {a: []} = foo;`.

- **no-eq-null: error**  
Při porovnávání s `null` se vyžaduje striktní porovnání `===`, `!==`.

- **no-eval: error**  
Zakazuje použití `eval`.

- **no-extra-bind: error**  
Podchytí použití `bind` když není potřeba.

- **no-fallthrough: error**  
Ve `switch case` vždy vyžaduje `break`. Při použití komentáře `// falls through` toto neplatí.

- **no-floating-decimal: error**  
U desetinných čísel nedovoluje začít tečkou, vyžaduje např. `-0.7` místo `-.7`.

- **no-global-assign: error**  
Zakazuje přepsat hodnotu globálních proměnných jako je `window`, `Object` a podobně.

- **no-implicit-coercion: error**  
Zakazuje nečitelné přetypování proměnné, např. `var a = !!foo;`.

- **no-implicit-globals: error**  
Proměnné deklarované v "global scope" musí být deklarovány jako vlastnosti `window`.

- **no-implied-eval: error**  
Zakazuje evaluaci kódu ve funkcích `setTimeout()`, `setInterval()` a `execScript()`.

- **no-iterator: error**  
Zakazuje použití `__iterator__`.

- **no-lone-blocks: error**  
Zakazuje samostatné bloky `{ ... }`, které nemají žádný význam.

- **no-loop-func: warn**  
Varuje před deklarací funkcí uvnitř `for` a `while`.

- **no-multi-spaces: error**  
Podchytí několik mezer za sebou (pokud nejsou použity k odsazení řádku).

- **no-new-func: error**  
Zakazuje vytváření funkce pomocí `Function()`.

- **no-new-wrappers: error**  
Zakazuje použití `new String()`, `new Number()` a `new Boolean()`.

- **no-octal: error**  
Zakazuje čísla začínající nulou, např. `071`.

- **no-proto: error**  
Zakazuje použití `__proto__`.

- **no-redeclare: ["warn", { "builtinGlobals": true }]**  
Varuje při opětovné deklaraci již vytvořené proměnné, včetně globálních proměnných.

- **no-return-assign: ["error", "always"]**  
Zakazuje přiřazení hodnoty do proměnné v `return`, např. `return foo = a + b;`.

- **no-script-url: error**  
Zakazuje URL začínající `javascript:`.

- **no-self-assign: error**  
Zakazuje přiřazení proměnné sama k sobě, např. `foo = foo`.

- **no-self-compare: error**  
Zakazuje porovnání proměnné sama k sobě, např. `if (foo === foo)`.

- **no-sequences: error**  
Zakazuje použití čárky, např. `a = b += 5, a + b;`. Toto neplatí pokud je výraz ve `for`, nebo obalený v závorkách.

- **no-unmodified-loop-condition: error**  
Zakazuje loopy s neměnnou podmínkou, např. `while (foo) { console.log(foo); }`.

- **no-unused-labels: error**  
Zakazuje labels, které nejsou v kódu využité, např. `A: while (i < 5) { i++; }`.

- **no-useless-call: error**  
Podchytí zbytečné volání metod `.call()` a `.apply()` v případě, že zavolání samotné funkce docílí toho samého.

- **no-useless-catch: error**  
Podchytí zbytečné použití `catch`.

- **no-useless-concat: error**  
Zakazuje zbytečné spojení stringů, např. `var foo = 'a' + 'b';`.

- **no-void: error**  
Zakazuje použití `void`.

- **no-with: error**  
Zakazuje použití `with`.

- **wrap-iife: ["error", "inside"]**  
Funkce, které se mají vykonat okamžitě, musí být obaleny závorkami, např. `(function () { ... })()`.

- **yoda: error**  
Při porovnávání zakazuje na první místo dát doslovnou hodnotu, např. `if ('red' == color)`.


### Variables

- **no-delete-var: error**  
Zakazuje použití `delete` na proměnnou.

- **no-label-var: error**  
Zakazuje stejné pojmenování label a proměnné.

- **no-shadow: warn**  
Hodí varování když se lokální proměnná pojmenuje stejně jako proměnná v "outer scope".

- **no-shadow-restricted-names: error**  
Zakazuje přepsání defaultních proměnných jako je `NaN`, `undefined` a podobně.

- **no-undef: error**  
Zakazuje použití proměnných, které nejsou výslovně deklarovány. Neplatí pro proměnné uvedené v `globals` v konfiguraci ESLintu.

- **no-undef-init: error**  
Zakazuje zbytečnou inicializaci proměnné jako `undefined`.

- **no-unused-vars: warn**  
Podchytí vytvořené, ale dále již nepoužité proměnné a funkce a vyhodí varování.


### Stylistic Issues

- **array-bracket-newline: ["error", "consistent"]**  
Vynucuje konzistentní použití přední `[` a zadní `]` hranaté závorky. Buď se nachází na stejném řádku jako jejich obsah, nebo na novém řádku.

- **array-bracket-spacing: ["error", "always"]**  
Vynucuje použití mezery uvnitř hranatých závorek, např. `[ foo, bar ]`.

- **array-element-newline: ["error", "consistent"]**  
Vynucuje konzistentní deklaraci elementů uvnitř pole `[]`. Buď jsou všechny na jednom řádku, nebo je každý odsazen na nový řádek.

- **block-spacing: ["error", "always"]**  
Vynucuje použití mezery uvnitř složených závorek, např. `{ foo = 10; }`.

- **brace-style: ["error", "stroustrup", { "allowSingleLine": true }]**  
Vyžaduje, aby byly bloky `if { ... }`, `else { ... }` a podobně vždy na novém řádku. Povoluje jednořádkové bloky.

- **camelcase: ["error", { "properties": "always" }]**  
Vyžaduje použití camelCase konvence při pojmenování proměnných.

- **comma-dangle: ["error", "always-multiline"]**  
Vyžaduje čárku za posledním elementem v objektu a poli.

- **comma-spacing: ["error", { "before": false, "after": true }]**  
Vyžaduje mezeru za čárkou a zakazuje mezeru před čárkou, např. `[ 1, 2, 3 ]`.

- **comma-style: ["error", "last"]**  
Při několikařádkové deklaraci vyžaduje umístění čárky na konci řádku.

- **eol-last: ["error", "never"]**  
Zakazuje prázdný řádek na konci souboru.

- **func-call-spacing: ["error", "never"]**  
Při volání funkce zakazuje mezeru mezi jménem funkce a závorkami, např. `doStuff()`.

- **func-name-matching: ["error", "always"]**  
Vyžaduje, aby se funkce jmenovala stejně jako proměnná, do které je přiřazena, např. `var foo = function foo () { ... }`.

- **func-paren-newline: ["error", "never"]**  
Zakazuje nový řádek v argumentech funkce.

- **indent: ["error", 4]**  
Nastavuje odsazení jako 4 mezery.

- **key-spacing: ["error", { "afterColon": true }]**  
Vyžaduje mezeru za dvojtečkou a zakazuje mezeru před dvojtečkou, např. `{ foo: 1, bar: 2 }`.

- **keyword-spacing: ["error", { "before": true, "after": true }]**  
Vyžaduje mezeru okolo klíčových slov jako `case`, `delete`, `if`, `function` apod.

- **linebreak-style: ["warn", "unix"]**  
Varuje pokud nejsou nové řádky kódovány unixovou konvencí `\n`.

- **lines-around-comment: ["error", { "beforeBlockComment": true, "afterBlockComment": true }]**  
Vyžaduje prázdné řádky kolem blokových komentářů `/* ... */`.

- **lines-between-class-members: ["error", "always"]**  
Vyžaduje prázdné řádky mezi funkcemi ve třídě.

- **max-statements-per-line: ["error", { "max": 3 }]**  
Nastavuje maximální počet příkazů na jednom řádku na 3.

- **multiline-ternary: ["error", "never"]**  
Zakazuje několikařádkové ternární výrazy.

- **new-cap: ["error", { "newIsCap": true }]**  
Vyžaduje, aby jména konstruktorů začínala velkým písmenem, např. `var friend = new Person();`.

- **new-parens: error**  
Zakazuje použití konstruktoru bez závorek, např. `var friend = new Person;`.

- **no-bitwise: error**  
Zakazuje bitwise operátory, např. `var x = y >> z;`.

- **no-lonely-if: error**  
Místo `else { if () { ... } }` vyžaduje `else if () { ... }`.

- **no-mixed-operators: error**  
Při mixování `&&` a `||` vyžaduje použití závorek `()`.

- **no-mixed-spaces-and-tabs: error**  
Při odsazení zakazuje mixování tabů a mezer.

- **no-nested-ternary: error**  
Zakazuje skládat ternární výrazy do sebe.

- **no-trailing-spaces: error**  
Zakazuje mezery na konci řádku.

- **no-unneeded-ternary: error**  
Zakazuje použití zbytečných ternárních operátorů, např. `(foo === 1 ? true : false)`.

- **no-whitespace-before-property: error**  
Zakazuje mezeru mezi objektem a vlastností, např. `foo. bar`.

- **nonblock-statement-body-position: ["error", "beside"]**  
Zakazuje nový řádek pokud není kód obalený složenými závorkami `{}`.

- **object-curly-newline: ["error", { "consistent": true }]**  
Vyžaduje konzistentní použití přední `{` a zadní `}` složené závorky. Buď se nachází na stejném řádku jako jejich obsah, nebo na novém řádku.

- **object-curly-spacing: ["error", "always"]**  
Vyžaduje použití mezery uvnitř složených závorek, např. `{ foo, bar }`.

- **object-property-newline: ["error", { "allowAllPropertiesOnSameLine": true }]**  
Vyžaduje konzistentní deklaraci vlastností uvnitř objektu `{}`. Buď jsou všechny na jednom řádku, nebo je každá odsazena na nový řádek.

- **operator-linebreak: ["error", "after"]**  
Při několikařádkové operaci vyžaduje umístění operátorů na konci řádku, např. `var foo = bar +`.

- **quote-props: ["error", "as-needed"]**  
Vlastnosti objektu vyžaduje bez uvozovek, např. `{ foo: 1, bar: 2}`. Povoluje je pouze u vlastností, kde jsou uvozovky potřeba, např. `{ 'foo-foo': 1, '2bar': 2}`.

- **quotes: ["error", "single"]**  
Vyžaduje používání jednoduchých místo dvojitých uvozovek, např. `var foo = 'bar';`.

- **semi: ["error", "always"]**  
Vyžaduje používání středníků na konci každého příkazu, např. `return { foo: 1 };`.

- **semi-spacing: ["error", { "before": false, "after": true }]**  
Vyžaduje mezeru za středníkem a zakazuje mezeru před středníkem, např. `var foo; var bar;`.

- **semi-style: ["error", "last"]**  
Vyžaduje umístění středníku na konci řádku.

- **space-before-blocks: ["error", "always"]**  
Vyžaduje mezeru před bloky kódu `{ ... }`.

- **space-before-function-paren: ["error", "always"]**  
Vyžaduje mezeru před závorkami funkce, např. `function foo () {}`.

- **space-in-parens: ["error", "never"]**  
Zakazuje mezeru v závorkách funkce, např. `foo( 'bar' );`.

- **space-infix-ops: error**  
Vyžaduje mezeru okolo operátorů `+`, `%` a podobně, např. `var sum = 1 + 2;`.

- **space-unary-ops: ["error", { "words": true, "nonwords": false }]**  
Vyžaduje mezeru okolo klíčových slov jako `new`, `delete`, `typeof` a podobně.

- **spaced-comment: ["error", "always"]**  
Vyžaduje mezeru na začátku komentáře, např. `// Comment`.

- **switch-colon-spacing: ["error", { "after": true, "before": false }]**  
Vyžaduje mezeru za dvojtečkou a zakazuje mezeru před dvojtečkou uvnitř `switch`, např. `case 'one': foo = 1;`.

- **template-tag-spacing: ["error", "always"]**  
Vyžaduje mezeru mezi funkcí a "template literal", např. ``var hello = func `Hello world`;``.


### ECMAScript 6

- **arrow-spacing: error**  
Vyžaduje mezery kolem `=>` v "arrow functions", např. `(foo) => { return foo + 1; }`.

- **constructor-super: error**  
Podchytí runtime errory při volání `super()`.

- **generator-star-spacing: error**  
U "generator functions" zakazuje mezeru za hvězdičkou a vyžaduje mezeru před hvězdičkou `function *generator () {}`.

- **no-class-assign: error**  
Zakazuje přepsání třídy, např. `class A { }; A = 0;`.

- **no-confusing-arrow: error**  
Zakazuje použití "arrow functions" v případech, kde se dají zaměnit za porovnání, např. `var x = a => 1 ? 2 : 3;`.

- **no-const-assign: error**  
Zakazuje přepsání proměnných definovaných pomocí `const`.

- **no-dupe-class-members: error**  
Zakazuje stejně pojmenované metody třídy.

- **no-new-symbol: error**  
Zakazuje `new` při volání `new Symbol( ... )`.

- **no-this-before-super: error**  
Zakazuje volání `this` a `super` předtím, než se zavolá `super()`.

- **no-useless-computed-key: error**  
Zakazuje zbytečné "computed keys", např. `var foo = {['a']: 'b'};`.

- **symbol-description: error**  
Při použití `Symbol` vyžaduje popis. `var foo = Symbol('some description');`.

- **template-curly-spacing: ["error", "always"]**  
Uvnitř proměnných `${}` v "template string" zakazuje mezery, např. ``let hello = `Hello, ${person.name}!`;``.

- **yield-star-spacing: ["error", "both"]**  
Vyžaduje mezery okolo `yield`, např. `function *generator () { yield * other(); }`.