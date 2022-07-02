# Regex Lookaround - [@abozhilov](https://twitter.com/abozhilov)

## Positive lookahead
`/▲(?=●)/` - matches `▲` if it is followed by `●` 

```js
'▲■●'.match(/▲■(?=●)/g); // ['▲■']
'▲■▲'.match(/▲■(?=●)/g); // null
```

## Positive lookbehind
`/(?<=▲)●/` - matches `●` if it is led by `▲`

```js
'▲■●'.match(/(?<=▲)■●/g); // ['■●']
'●■●'.match(/(?<=▲)■●/g); // null
```

## Negative lookahead
`/▲(?!●)/` - matches `▲` if it is not followed by `●`

```js
'▲■▲'.match(/▲■(?!●)/g); // ['▲■']
'▲■●'.match(/▲■(?!●)/g); // null
```

## Negative lookbehind
`/(?<!▲)●/` - matches `●` if it is not led by `▲`

```js
'●■●'.match(/(?<!▲)■●/g); // ['■●']
'▲■●'.match(/(?<!▲)■●/g); // null
```