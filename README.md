# postcss-sample

Run:

```bash
yarn start
```

> src/index.postcss
```postcss
@define-mixin btn $name {
  $(name) {
    &.after, &::after {
      color: red;
      @mixin-content;
    }

    &:focus, &.focus {
      color: green;
    }

    &.active, &:active {
      color: blue;
    }

  }
}

@mixin btn .btn-bar {
    font-size: 12px;
}
```

> dist/style.css
```css
.btn-bar.after, .btn-bar::after {
    color: red;
    font-size: 12px;
}
.btn-bar:focus, .btn-bar.focus {
    color: green;
}
.btn-bar.active, .btn-bar:active {
    color: blue;
}
```
