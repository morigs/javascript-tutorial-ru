Несмотря на то, что меню более-менее прилично отображается, эта вёрстка совершенно не семантична.

Ошибки:

1. Во-первых, меню представляет собой *список элементов*, а для списка существует тег `LI`.

    **Семантический подход -- это когда теги используются по назначению.** Для элементов списка `<li>`, для адреса `<address>`, для заголовка таблицы `<th>` и т.п.
2. Во-вторых, класс `rounded-horizontal-blocks` показывает, что содержимое должно быть *оформлено* как скругленные горизонтальные блоки. Любой класс, отражающий оформление, несемантичен.

    **Правильно -- чтобы класс был *смысловым***. Например, `<ul class="menu">` будет говорить о том, что смысл элемента -- "меню".
3. В-третьих, элемент `.vertical-splitter`. Здесь класс вполне семантичен, этот элемент списка является вертикальным разделителем, так что здесь всё в порядке. Но на этот раз несемантичность -- в содержимом.

    **Мы, по возможности, стараемся, чтобы HTML содержал именно информацию, а символ вертикальной черты`|` выполняет чисто оформительскую функцию.**

    Поэтому от него следует либо вообще избавиться, либо переместить в CSS при помощи `::before`.

И, наконец, это не обязательно и не ошибка, но обычно элементы, которые являются ссылками или кнопками, оформляют в `<a>` или `<button>`.

Вариант ниже -- семантичен:

```html
<ul class="menu">
  <li class="menu__item"><a href="#">Главная</a></li>
  <li class="menu__vertical-splitter"></li>
  <li class="menu__item"><a href="#">Товары</a></li>
  <li class="menu__item"><a href="#">Фотографии</a></li>
  <li class="menu__item"><a href="#">Контакты</a></li>
</ul>
```

Дополнительно, классы помечены префиксом компонента, на тот случай, если в заголовках появится произвольный HTML.

