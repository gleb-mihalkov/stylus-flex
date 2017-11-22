# Flexbox block for Stylus.

## Подключение

```bash
bower install --save https://github.com/gleb-mihalkov/stylus-flex.git
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

## API

### .flex

#### Модификаторы по умолчанию

* *--align-[left|top|right|bottom|center|between|around]* - Расположение элементов по горизонтальной оси.

* *--v-align-[top|left|bottom|right|center|stretch|baseline]* - Расположение элементов по вертикальной оси.

* *--w-align-[top|left|bottom|right|center|stretch|between|around]* - Расположение строк при переносе элементов.

* *--vertical* - Меняет местами горизонтальную ось и вертикальную.

* *--wrap* - Разрешает перенос элементов на новую строку.

#### .flex__item

* *--align-[top|left|bottom|right|center|stretch|baseline]* - Расположение элемента по вертикальной оси.

* *--size-[grow|shrink|auto]* - Задает размер элемента. *grow* - элемент растянется на оставшееся свободное простанство по горизонтальной оси, *shrink* - элемент сожмется по горизонатли, если свободное пространство кончилось, *auto* - и то, и другое.

* *--pulled-[left|right|center|top|bottom]* - Прижимает элемент в нужную сторону.