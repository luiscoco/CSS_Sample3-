# CSS_Sample4-scss

## main.scss

```scss
@use "_variables" as *;
@use "_mixins" as *;
@use "_placeholders" as *;

.parent {
  background-color: $parent-bgColor;
  @include size(100px, 150px);
  @include center(center);
  @extend %border;

  &--round {
    background-color: $parent-bgColor;
    @include size(100px);
    @include center(end, end)
  }
}

.child {
  background-color: $child-bgColor;
  @include size(50px, 25px);
  @extend %border;
  @include scaleOnHover;

  &--round {
    background-color: $child-bgColor;
    @include size(50px);
    @include scaleOnHover;
  }
}
```
