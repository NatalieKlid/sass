# sass

# mixins

allow to create style blocks that can be used for different selectors later on

## syntacsis

```
    @mixin styleName($fontSize: 50px) {
        font-size: $fontSize;
        color: red;
        font-weight: bold;
    }

    .someClassSelector {
        @include styleName(30px); // here all styles from styleName mixin will be applied
    }
```

# extend

allows to inherit styles from some selector

## syntacsis

```
.someClass {
    color: red;
    font-size: 12px;
    &:hover {
        color: purple;
    }
}

.classThatWillInheritStyles {
    @extend .someClass // here styles will be the same as for .someClass; Note: no nested selectors allowed
}
```

# functions
## syntacsis

```
@function functionName($fontSize: 10px){
    @return $fontSize * 2;
}

.someClass {
    font-size: functionName(20px); // result: 40px
}
```

## Built-in functions

```
    color: lighten(red, 20%); // lightens the color provided as 1st parameter by 20%

    color: darken(red, 20%); // darkens the color provided as 1st parameter by 20%

    color: transparentize(red, .8); // sets opacity, 2nd parameter is a number from 0 to 1; the opacity is equal to 1 - 2nd parameter

    color: mix(blue, green); // mixes the colors provided as parameters; accepts percentage as 3rd parameter which stands for the percentage of the 1st color in the mixed one
```

[Full list of functions](https://web.archive.org/web/20180208190131/http://sass-lang.com/documentation/Sass/Script/Functions.html)

[Functions cheatsheet at github](https://gist.github.com/AllThingsSmitty/3bcc79da563df756be46)

