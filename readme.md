# Верстка

## Верстка блока

Готовый бандл в папке **prod-part-1**.
Исходники в папке **src**.

Чтобы собрать бандл заново, нужно сначала установить зависимости, затем запустить сборку:

    npm install
    npm run prod


## Таблица на странице

Готовое решение в папке **prod-part-2**.

> В текст статьи на странице с адаптивной версткой менеджеры добавили таблицу. На десктопе таблицы выглядят хорошо, но на мобиле - появляется горизонтальный скролл, верстка едет. Что делать?

### Кратко о решении
Основная идея — развернуть все строки таблицы в один столбец.

- Прежде всего, почистил код от инлайн-стилей и пустых тегов. Перенес стили в CSS файл.
- Затем добавил медиазапрос с границей по max ширине. Установил для всех строк таблицы <tr> режим отображения *flex*, а для всех ячеек задал ширину *100%*.
- Во флексе склеивание границ ячеек *(border-collapse)* не работает, поэтому отдельным правилом поправил границы ячеек.
