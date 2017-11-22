# Flexbox block for Stylus.

## Подключение

```bash
```

## Использование

```stylus
@import '../bower_components/stylus-flex/src/flex'

.flex
  flex-space 10px 20px 24px
  flex-v-space 24px
  flex-columns 2 3 4
```

```html
<div class="flex flex--v-align-stretch flex--space-px-24 flex--v-space-px-24 flex--columns-3">
  <div class="flex__item"></div>
  <div class="flex__item"></div>
  <div class="flex__item"></div>
  <div class="flex__item"></div>
  <div class="flex__item"></div>
  <div class="flex__item"></div>
</div>
```

