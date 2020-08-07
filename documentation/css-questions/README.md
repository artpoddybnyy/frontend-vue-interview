# CSS questions
1. Как отображать картинки base64 
 ::: answer
 * `background-image: url("")`, 
 * `<img src="" />` 
 * `data:image/png;base64, код`
 :::
 2. Что такое **svg** и как анимировать **svg**
 3. Приоритет индексирования анимации **transform** и z-index
 4. Как отследить анимацию **transition**, **animation** (начало, окончание)
 5. Тег `<pre>`, что он делает
 6. Что такое **srcset**, **dataset** атрибуты на елементах
 7. Как выровнять елемнт в контейнере по вертикали и горизонтали
 8. Какую анимацию и как использовать  **transition**, **animation** в чем отличие, можно ли остановить анимацию. 
 Что такое **transform**, **transform-origin**. **transform-origin** у **svg**
 ::: answer
 * `animation-play-state:paused;`
 * transform-origin у svg 0% 0% по умолчанию это цент svg
 :::
9. Какое поведение будет при изменении ширины контейнера у flex items?<br>
Как изменить порядок переноса flex item 
::: answer
По умолчанию елементы не переносятся flex `revers-wrap`
:::
10. Как растянуть флекс елементы на высоту контейнера, как растянуть отдельный елемент по ширене?
::: answer
* align-content: stretch
* flex-grow: 1; растянит один елемт на всю ширину или все елементы заполнят всю ширину
:::
11. Свойства `object-fit` и `object-position`
12. Какие `input types` можно назвать
13. Какие `button types` можно назвать и тип `reset` как очистить форму
14. Структура елемента `margin` `outline` `border` `padding` `element content`
15. Как сделать двойную рамку у елемента, что такое  `outline-offset`, 
16. Что такое `border-image` для чего можно использовать
17. Что такое `clip-path` для чего можно использовать
18. Сбособы сделать круг из фигуры, как сделать многоугольную кнопку
19. Значение верхних и нижних отступов, заданное в %, считается относительно ширины, а не высоты родительского блока
20. `vertical-align` если применим к инлайн- или инлайн-блочным элементам — выровняется сам блок, причем относительно соседних инлайновых и инлайн-блочных элементов. Можно задавать в еденицах измерения
21. `text-indent` отсуп текста абзац, работает только на блоках. Если задать отрицательный и padding получиться отступ всего текст кроме первой строки 
22. `page-break-before` Добавляет разрыв страницы при печати документа перед заданным элементом.
23. `box-sizing: border-box` — в данном случае браузер включает отступы padding и рамку border в общую ширину/высоту элемента.
24. Если высота внешнего блока вычисляется по содержимому, то высота в `%` для дочернего не работает, и заменяется на `height: auto`. Кроме случая, когда у элемента стоит `position: absolute`.
Если у родительского элемента не установлено `height`, а указано `min-height`, то, чтобы дочерний блок занял `100% высоты`, нужно родителю поставить свойство `height: 1px;`
25. Как сделать скролл для елемента
```css
div {
    overflow: scroll;
    max-height: calc(100vh - 113px);
}
```