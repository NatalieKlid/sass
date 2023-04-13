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