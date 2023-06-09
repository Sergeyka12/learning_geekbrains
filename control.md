# Краткое руководство по Маркдауну (Markdown)

текст редактированный, на основе [Краткое руководство по Маркдауну](https://paulradzkov.com/2014/markdown_cheatsheet/)
 
## Абзацы

Абзацы создаются при помощи пустой строки. Если вокруг текста сверху и снизу есть пустые строки, то текст превращается в абзац.

Чтобы сделать перенос строки вместо абзаца,  
нужно поставить два пробела в конце предыдущей строки.

## Заголовки

Заголовки отмечаются диезом `#` в начале строки, от одного до шести. Например:

# Заголовок первого уровня #
## Заголовок h2
### Заголовок h3
#### Заголовок h4
##### Заголовок h5
###### Заголовок h6

В декоративных целях заголовки можно «закрывать» с обратной стороны.

## Списки

Для разметки неупорядоченных списков можно использовать или `*`, или `-`, или `+`:

- элемент 1
- элемент 2
- элемент ...

Вложенные пункты создаются четырьмя пробелами перед маркером пункта:

* элемент 1
* элемент 2
    * вложенный элемент 2.1
    * вложенный элемент 2.2
* элемент ...

Упорядоченный список:

1. элемент 1
2. элемент 2
    1. вложенный
    2. вложенный
3. элемент 3
4. элемент 4

На самом деле не важно как в коде пронумерованы пункты, главное, чтобы перед элементом списка стояла цифра (любая) с точкой. Можно сделать и так:

0. элемент 1
0. элемент 2
0. элемент 3
0. элемент 4

Список с абзацами:

* Раз абзац.

* Два абзац. 

* Три абзац. 

* 
    Четыре абзац (Четыре пробела в начале или один tab).

## Цитаты

Цитаты оформляются как в емейлах, с помощью символа `>`.

> Это блок-цитата 

> текст
> текст
>
> текст
>> текст вложенной цитаты текст вложенной цитаты текст вложенной цитаты

>текст
цитаты

Или более ленивым способом, когда знак `>` ставится перед каждым элементом цитаты, будь то абзац, заголовок или пустая строка:

> текст        цитаты текст цитаты текст цитаты текст цитаты текст цитаты текст цитаты текст цитаты
>
> текст цитаты текст цитатытекст цитаты текст цитатытекст цитаты текст цитатытекст цитаты текст цитаты

Выход из текста цитаты 

В цитаты можно помещать всё что угодно, в том числе вложенные цитаты:

> ## Это заголовок.
>
> 1. Это первый элемент списка.
> 2. Это второй элемент списка.
>
> > Вложенная цитата.
>
> >> Вложенная цитата второго уровня. Here's some example code
>        return shell_exec("echo $input | $markdown_script")
## Горизонтальная черта

ЧЕРТА создается тремя звездочками или тремя подчеркиваниями, тремя дефисами.

***
___
---

## Ссылки
Это встроенная [ссылка с title элементом](http://example.com/link "Я ссылка"). Это — [без title](http://example.com/link).

А вот [пример][1] [нескольких][2] [ссылок][id] с разметкой как у сносок. Прокатит и [короткая запись][] без указания id.

[1]: http://example.com/ "Optional Title Here"
[2]: http://example.com/some
[id]: http://example.com/links (Optional Title Here)
[короткая запись]: http://example.com/short

Вынос длинных урлов из предложения способствует сохранению читабельности исходника. Сноски можно располагать в любом месте документа.

## Шрифты

Выделять слова можно при помощи `*` и `_`. Одним символ для наклонного текста, два символа для жирного текста, три — для наклонного и жирного одновременно.

Например, это _italic_ и это тоже *italic*. А вот так уже __strong__, и так тоже **strong**. А так ***жирный и наклонный*** одновременно.

## Зачеркивание

В зачеркивание текста: две тильды `~` до и после текста.

~~Зачеркнуто~~

## Картинки

Картинка без `описания` текста

![](150x100.png)

![Картинка](200x100.png)
![Картинка](250x100.png)

Картинки-ссылки:

[![Alt text](//placehold.it/150x100)](http://example.com/)

## Таблицы

В чистом Маркдауне нет синтаксиса для таблиц, а в GFM (Github Flavoured Markdown) есть.

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

Для красоты можно и по бокам линии нарисовать:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

Можно управлять выравниванием столбцов при помощи двоеточия.

| Left-Aligned  | Center Aligned  | Right Aligned |
|:------------- |:---------------:| -------------:|
| col 3 is      | some wordy text |     **$1600** |
| col 2 is      | centered        |         $12   |
| zebra stripes | are neat        |        ~~$1~~ |

Внутри таблиц можно использовать ссылки, наклонный, жирный или зачеркнутый текст.
