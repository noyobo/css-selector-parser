[css-selector-parser](../../README.md) / [Exports](../modules.md) / AstFormulaOfSelector

# Interface: AstFormulaOfSelector

Pseudo-class formula of selector value. `a` is multiplier of `n` and `b` us added on top. Formula: `an + b`.
Formula is followed by `of` keyword and then goes a CSS selector.
For instance `:nth-child(2n + 1 of div)` ->
`{type: 'AstPseudoClass'..., argument: {type: 'FormulaOfSelector', a: 2, b: 1, selector: {type: 'Selector', rules: [{type: 'Rule', tag: {type: 'TagName', name: 'div'}}]}}}`.
Generated by [ast.formulaOfSelector](AstFactory.md#formulaofselector).

**`See`**

https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child#functional_notation

## Table of contents

### Properties

- [a](AstFormulaOfSelector.md#a)
- [b](AstFormulaOfSelector.md#b)
- [selector](AstFormulaOfSelector.md#selector)
- [type](AstFormulaOfSelector.md#type)

## Properties

### a

• **a**: `number`

Multiplier of `n`.

___

### b

• **b**: `number`

Constant added to `a*n`.

___

### selector

• **selector**: [`AstRule`](AstRule.md)

Selector that goes after formula (i.e. `"div -> span"` in case of `":nth-child(2n + 1 of div > span)"`

___

### type

• **type**: ``"FormulaOfSelector"``