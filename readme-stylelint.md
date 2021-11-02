# Stylelint

Naše defaultní pravidla jsou definována v [`stylelint-default.json`](stylelint-default.json). Pravidla pro projekt upravuj vždy přímo v daném projektu v souboru `stylelint.json`.

Kompletní dokumentace stylelint pravidel zde: https://stylelint.io/user-guide/rules/


## Naše pravidla ve zkratce

### Possible Errors

- **block-no-empty: true**  
Zákaz prázdných bloků `{ }`.

- **color-no-invalid-hex: true**  
Zákaz nevalidních hexa barev `#ya3`.

- **comment-no-empty: true**  
Zákaz prázdných komentářů `/* */`.

- **declaration-block-no-duplicate-properties: [ true, { "ignore": [ "consecutive-duplicates-with-different-values" ] } ]**  
Zákaz duplicitních vlastností v jednom bloku. Neplatí při progressive enhancement, např. `width: calc(100% - 30px); width: 90%;`.

- **declaration-block-no-shorthand-property-overrides: true**  
Zákaz obecných vlastností, které přepisují specifické vlastnosti, např. `padding-left: 10px; padding: 20px;`.

- **font-family-no-duplicate-names: true**  
Zákaz duplicitních názvů fontu `font-family: Arial, Arial;`.

- **font-family-no-missing-generic-family-keyword: true**  
Definice fontu musí vždy obsahovat obecné klíčové slovo, např. `font-family: Arial, sans-serif;`.

- **function-calc-no-unspaced-operator: true**  
Kolem operátorů v `calc()` musí být vždy mezera, např. `calc(10% + 2px)`.

- **function-linear-gradient-no-nonstandard-direction: true**  
Zákaz nevalidních hodnot v `linear-gradient()`.

- **keyframe-declaration-no-important: true**  
Zákaz použití `!important` uvnitř `@keyframes`.

- **media-feature-name-no-unknown: true**  
Zákaz použití neznámých hodnot v `@media`.

- **no-duplicate-at-import-rules: true**  
Zákaz duplicitních `@import`ů.

- **no-duplicate-selectors: true**  
Zákaz duplicitních selektorů.

- **no-empty-source: true**  
Zákaz prázdných souborů.

- **no-extra-semicolons: true**  
Zákaz přebytečných středníků `color: red;;`.

- **no-invalid-double-slash-comments: true**  
Zákaz jednořádkových komentářů `//` v čistém CSS.

- **property-no-unknown: true**  
Zákaz neznámých vlastností, např. `colorr: red;`.

- **selector-pseudo-class-no-unknown: true**  
Zákaz neznámých pseudo tříd, např. `a:hoover { ... }`.

- **selector-pseudo-element-no-unknown: true**  
Zákaz neznámých pseudo elementů, např. `a::pseudo { ... }`.

- **selector-type-no-unknown: true**  
Zákaz neznámých HTML elementů, např. `headr { ... }`.

- **string-no-newline: true**  
Zákaz odřádkování uprostřed stringu bez escape.

- **unit-no-unknown: true**  
Zákaz neznámých jednotek, např. `width: 1pixel;`.


### Limit language features

- **number-max-precision: 3**  
Omezení míst za desetinnou čárkou na maximálně 3, např. `width: 5.125%;`.

- **declaration-block-single-line-max-declarations: 1**  
Omezení počtu deklarací v jednořádkovém bloku na 1, např. `a { color: red; }`.

- **selector-max-empty-lines: 0**  
Zákaz prázdných řádků v selektoru.

- **selector-max-universal: 2**  
V jednom selektoru lze využít `*` maximálně 2x, např. `*.foo * { ... }`.

- **no-unknown-animations: true**  
Zákaz animací, které nejsou definovány.


### Stylistic issues

- **color-hex-case: lower**  
Zákaz psaní hexa barev velkými písmeny, např. `color: #FEdA5b;`.

- **font-family-name-quotes: always-where-recommended**  
Vyžaduje uvozovky kolem názvu fontů, kde je to doporučeno, např. `font-family: "Times New Roman", serif;`.

- **function-comma-space-after: always**  
Vyžaduje mezeru za čárkou ve funkci, např. `transform: translate(1, 1);`.

- **function-comma-space-before: never**  
Zákaz mezery před čárkou ve funkci, např. `transform: translate(1 ,1);`.

- **function-max-empty-lines: 0**  
Zákaz prázdných řádků ve funkci.

- **function-parentheses-space-inside: never**  
Zákaz mezery uvnitř závorek ve funkci, např. `transform: translate( 1, 1 );`.

- **function-whitespace-after: always**  
Vyžaduje mezeru za funkcí, např. `transform: translate(1, 1) scale(3);`.

- **number-leading-zero: always**  
Vyžaduje, aby desetinná čísla začínala nulou, např. `line-height: 0.5;`.

- **number-no-trailing-zeros: true**  
V desetinných číslech zakazuje nuly na konci, např. `top: 0.500px;`.

- **string-quotes: double**  
Vyžaduje použití dvojitých uvozovek, např. `a[id="my-link"]`.

- **length-zero-no-unit: true**  
Zákaz použití jednotek pro nulové hodnoty, např. `margin-top: 0px;`.

- **unit-case: lower**  
Zákaz psaní jednotek velkými písmeny, např. `width: 10REM;`.

- **value-keyword-case: lower**  
Zákaz psaní klíčových slov velkými písmeny, např. `display: Block;`.

- **value-list-comma-space-after: always**  
Vyžaduje mezeru za čárkou v hodnotě, např. `background-size: cover, 10px 5px;`.

- **value-list-comma-space-before: never**  
Zakazuje mezeru před čárkou v hodnotě, např. `background-size: cover ,10px 5px;`.

- **value-list-max-empty-lines: 0**  
Zákaz prázdných řádků v hodnotě.

- **property-case: lower**  
Zákaz psaní vlastností velkými písmeny, např. `DISPLAY: block;`.

- **declaration-bang-space-after: never**  
Zákaz mezery za `!important`, např. `color: pink!important ;`.

- **declaration-bang-space-before: always**  
Vyžaduje mezeru před `!important`, např. `color: pink !important;`.

- **declaration-colon-space-after: always**  
Vyžaduje mezeru za dvojtečkou v deklaraci, např. `color: red;`.

- **declaration-colon-space-before: never**  
Zákaz mezery před dvojtečkou v deklaraci, např. `color :red;`.

- **declaration-block-semicolon-newline-after: always**  
Za středníkem vyžaduje nový řádek.

- **declaration-block-semicolon-space-after: always-single-line**  
Zákaz mezery za středníkem, např. `width: auto; `.

- **declaration-block-semicolon-space-before: never**  
Zákaz mezery před středníkem, např. `width: auto ;`.

- **declaration-block-trailing-semicolon: always**  
Vyžaduje středník i za posledním pravidlem v bloku.

- **block-closing-brace-newline-after: always**  
Za ukončením bloku `}` vyžaduje nový řádek.

- **block-closing-brace-newline-before: always-multi-line**  
Před ukončením bloku `}` vyžaduje nový řádek, pokud obsahuje víc jak jedno pravidlo.

- **block-opening-brace-space-before: always**  
Před začátkem bloku `{` vyžaduje mezeru, např. `a { padding: 5px; }`.

- **selector-attribute-brackets-space-inside: never**  
Zákaz mezer uvnitř selektoru atributu `[]`, např. `a[ target="_blank" ]`.

- **selector-attribute-operator-space-after: never**  
Zákaz mezery za operátorem uvnitř selektoru atributu, např. `a[target= "_blank"]`.

- **selector-attribute-operator-space-before: never**  
Zákaz mezery před operátorem uvnitř selektoru atributu, např. `a[target ="_blank"]`.

- **selector-attribute-quotes: always**  
Vyžaduje uvozovky kolem hodnoty v selektoru atributu, např. `a[target="_blank"]`.

- **selector-combinator-space-after: always**  
Vyžaduje mezeru za kombinačním znamínkem, např. `div+ div`.

- **selector-combinator-space-before: always**  
Vyžaduje mezeru před kombinačním znamínkem, např. `div +div`.

- **selector-descendant-combinator-no-non-space: true**  
Povoluje pouze mezeru jako oddělovací znak v selektoru.

- **selector-pseudo-class-case: lower**  
Zákaz psaní pseudo tříd velkými písmeny, např. `a:Hover`.

- **selector-pseudo-class-parentheses-space-inside: never**  
Zakazuje mezery v závorkách u pseudotřídy, např. `div:not( #foo )`.

- **selector-pseudo-element-case: lower**  
Zákaz psaní pseudo elementů velkými písmeny, např. `div:BEFORE`.

- **selector-type-case: lower**  
Zákaz psaní elementů velkými písmeny, např. `MAIN > section`.

- **selector-list-comma-newline-before: never-multi-line**  
Zákaz nového řádku před čárkou v selektorech.

- **selector-list-comma-newline-after: always**  
Vyžaduje nový řádek za čárkou v selektorech.

- **media-feature-colon-space-after: always**  
Vyžaduje mezeru za dvojtečkou v media query, např. `@media (max-width: 600px)`.

- **media-feature-colon-space-before: never**  
Zákaz mezery před dvojtečkou v media query, např. `@media (max-width :600px)`.

- **media-feature-name-case: lower**  
Zákaz psaní media queries velkými písmeny, např. `@media (MIN-WIDTH: 90rem)`.

- **media-feature-parentheses-space-inside: never**  
Zákaz mezer v závorkách media query, např. `@media ( max-width: 360px )`.

- **media-feature-range-operator-space-after: always**  
Vyžaduje mezeru za operačním znamínkem v media query, např. `@media (width>= 600px)`.

- **media-feature-range-operator-space-after: always**  
Vyžaduje mezeru před operačním znamínkem v media query, např. `@media (width >=600px)`.

- **media-query-list-comma-space-after: always**  
Vyžaduje mezeru za čárkou v media query, např. `@media screen, print`.

- **media-query-list-comma-space-before: never**  
Zákaz mezery před čárkou v media query, např. `@media screen ,print`.

- **at-rule-name-case: lower**  
Zákaz psaní @ pravidel velkými písmeny, např. `@CHARSET 'UTF-8'`.

- **at-rule-name-space-after: always**  
Vyžaduje mezeru za @ pravidly, např. `@media screen`.

- **at-rule-semicolon-newline-after: always**  
Vyžaduje nový řádek za středníkem v @ pravidlech.

- **at-rule-semicolon-newline-before: never**  
Zákaz nového řádku před středníkem v @ pravidlech.

- **comment-whitespace-inside: always**  
Vyžaduje mezeru uvnitř komentářů, např. `/* Comment */`.


### General

- **indentation: tab**  
Odsazení pomocí tabů.

- **linebreaks: unix**  
Odřádkování pomocí `\n`.

- **max-empty-lines: 3**  
Omezení počtu po sobě jdoucích prázdných řádků na max. 3.

- **no-eol-whitespace: true**  
Zákaz mezer na konci řádku.

- **no-missing-end-of-source-newline: true**  
Na konci souboru musí být prázdný řádek.

- **no-empty-first-line: true**  
Soubor nemůže začínat prázdným řádkem.


### SCSS specific

- **scss/at-rule-no-unknown: true**  
Zákaz použití neznámých `@pravidel`.

- **scss/at-mixin-argumentless-call-parentheses: always**  
Vyžaduje použití závorek u `@mixin` i pokud nemá argumenty, např. `@mixin foo()`.

- **scss/at-mixin-parentheses-space-before: never**  
Zákaz mezery před závorkami u `@mixin`, např. `@mixin foo ()`.

- **scss/dollar-variable-colon-space-after: always**  
U proměnné vyžaduje mezeru za dvojtečkou, např. `$foo: 10px;`.

- **scss/dollar-variable-colon-space-before: never**  
Zákaz mezery před dvojtečkou u proměnné, např. `$foo :10px;`.

- **scss/dollar-variable-no-missing-interpolation: true**  
Upozorní na chybějící interpolaci proměnné tam, kde je to potřeba.

- **scss/double-slash-comment-whitespace-inside: always**  
Vyžaduje mezeru v inline komentáři za lomítky, např. `// comment`.

- **scss/operator-no-unspaced: true**  
Vyžaduje mezeru kolem operátorů, např. `width: $foo + 5px;`.

- **scss/selector-no-redundant-nesting-selector: true**  
Zákaz redundantních selektorů, např. `p { & a { ... } }`.

- **scss/no-duplicate-dollar-variables: true**  
Zákaz duplicitních proměnných.


### Properties order

Související CSS vlastnosti automaticky držíme u sebe a řadíme je dle pluginu [`stylelint-config-rational-order`](https://github.com/constverum/stylelint-config-rational-order#stylelint-config-rational-order).