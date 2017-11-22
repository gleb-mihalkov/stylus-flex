# Flexbox block for Stylus.

Блок *flexbox*.

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

Элемент flexbox блока.

* *--align-[top|left|bottom|right|center|stretch|baseline]* - Расположение элемента по вертикальной оси.

* *--size-[grow|shrink|auto|full]* - Задает размер элемента. *grow* - элемент растянется на оставшееся свободное простанство по горизонтальной оси, *shrink* - элемент сожмется по горизонатли, если свободное пространство кончилось, *auto* - и то, и другое. *full* - делает ширину на 100%.

* *--pulled-[left|right|center|top|bottom]* - Прижимает элемент в нужную сторону.

#### Миксин flex-space

Добавляет дополнительные модификаторы для блока `.flex`. Задают расстояние между элементами блока. Использование:

```stylus
.flex
  // будут добавлены отступы в 10px, 20px и 30px
  flex-space 10px 20px 30px
```

* *--space-[px|per|em|pt|rem...]-{value}* - Добавляет расстояние между всеми элементами блока по горизонтали.

#### Миксин flex-v-space

Добавляет дополнительные модификаторы для блока `.flex`. Задают расстояние между элементами блока. Использование:

```stylus
.flex
  // будут добавлены отступы в 10px, 20px и 30px
  flex-v-space 10px 20px 30px
```

* *--v-space-[px|per|em|pt|rem...]-{value}* - Добавляет расстояние между всеми элементами блока по вертикали.

#### Миксин flex-columns

Добавляет дополнительные модификатор для блока `.flex` и элементов `.flex__item`. Задает размеры элементов по горизонтали. Использование:

```stylus
.flex
  // будут добавлены размеры элементов двух, трех и шестиколоночной сетки.
  flex-columns 2 3 6
```

* *.flex--columns-{count}* - Делает блок count-колоночной сеткой.

* *.flex__item--size-{size}-{count}* - Задает размер элемента в count-колоночной сетке.