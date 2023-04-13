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