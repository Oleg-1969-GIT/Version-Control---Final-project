# Инструкция для работы с Markdown

## Выделение текста

Чтобы выделить текст курсивом необходимо выделить его звездочками (*) или знаком нижнего подчеркивания (_). Например, *вот так* или *вот так*.

Чтобы зачеркнуть текст, необходимо выделить его с двух сторон двойными "тильдами" (~). Например, ~~вот так~~.

Чтобы выделить текст полужирным, необходимо обрамить его двойными звёздочками (**) или двойным знаком нижнего подчеркивания (_). Например,**вот так** или **вот так**.

Альтернативные способы выделения текста жирным или курсивом нужны для того, чтобы можно было совмещать оба эти способа. Например, __текст может быть выделен курсивом и при этом быть **полужирным**__.

---

## Списки

Чтобы добавить ненумерованные списки необходимо выделить пункты звездочкой (*) или знаком (+). Например, вот так:

* Элемент 1
* Элемент 2
* Элемент 3

+ Элемент 4

Вложенные пункты (низшей иерархии) создаются четырьмя пробелами (или "tab") перед маркером пункта:  

* Элемент 1
* Элемент 2, варианты:
  * вложенный элемент 1
  * вложенный элемент 2

Чтобы добавить нумерованные списки, необходимо пункты просто пронумеровать. Например, вот так:

1. Первый пункт
3. Второй пункт

При этом не важно, какая цифра будет стоять в коде. Главное, чтобы перед элементом списка стояла цифра (любая) с точкой. Можно и вот так:

0. Первый
0. Второй
0. Третий

---

## Изображения

Чтобы вставить изображение в текст, достаточно сделать следующее:
![Привет, это Барсик!](Барсик.jpg)

Картинки-ссылки:

[![Вид на горы](Горы.jpeg)](https://the-challenger.ru/wp-content/uploads/2020/08/snimok-ekrana-2020-08-06-v-10.49.08.jpg)

---

## Ссылки  

Это встроенная [ссылка с title элементом](https://paulradzkov.com/2014/markdown_cheatsheet/ "Краткая инструкция"). Это — [без title](https://paulradzkov.com/2014/markdown_cheatsheet/).

А вот [пример](1) [нескольких](2) [ссылок](id) с разметкой как у сносок:

(1) : <http://example.com/> "Optional Title Here"  
(2) : <http://example.com/some>  
(id) : <http://example.com/links> (Optional Title Here)  

Вынос длинных урлов из предложения способствует сохранению читабельности исходника. Сноски можно располагать в любом месте документа.

---

## Работа с таблицами

В чистом Markdown нет синтаксиса для таблиц, а в GFM есть.

First Header|Second Header
------------|-------------
Content Cell|Content Cell
Content Cell|Content Cell

Для красоты можно нарисовать линии по бокам и выровнять столбцы при помощи двоеточий (:).

| First Header | Second Header | Third Header | 
|:--------|:----------:|---------:|
|Content Cell|Content Cell|[Content Cell]()|
|~~Зачеркнутый текст~~|**Полужирный**|*Наклонный текст*|

Внутри таблиц можно также использовать ссылки, наклонный, зачеркнутый и полужирный текст.

---

## Цитаты

Цитаты оформляются как в емейлах, с помощью символа (>):

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

Или более ленивым способом, когда знак (>) ставится перед каждым элементом цитаты, будь то абзац, заголовок или пустая строка:

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

В цитаты можно помещать всё что угодно, в том числе вложенные цитаты:

> ## This is a header.
>
> 1.   This is the first list item.
> 2.   This is the second list item.
>
> > Вложенная цитата.
>
> Here's some example code:
>
>     return shell_exec("echo $input | $markdown_script");

---

## Исходный код

В чистом Маркдауне блоки кода отбиваются 4 пробелами в начале каждой строки.

Но в GitHub-Flavored Markdown (сокращенно GFM) есть более удобный способ: ставим по три апострофа до и после кода. Также можно указать язык исходного кода.

```html
<nav class="nav nav-primary">
  <ul>
    <li class="tab-conversation active">
      <a href="#" data-role="post-count" class="publisher-nav-color" data-nav="conversation">
        <span class="comment-count">0 комментариев</span>
        <span class="comment-count-placeholder">Комментарии</span>
      </a>
    </li>
    <li class="dropdown user-menu" data-role="logout">
      <a href="#" class="dropdown-toggle" data-toggle="dropdown">
        <span class="dropdown-toggle-wrapper">
          <span>
            Войти
          </span>
        </span>
        <span class="caret"></span>
      </a>
    </li>
  </ul>
</nav>
```

Самое приятное, что в коде не нужно заменять угловые скобки `< >` и амперсанд `&` на их html-сущности.

### Инлайн код

Для вставки кода внутри предложений нужно заключать этот код в апострофы. Пример:
`<html class="ie no-js">`

Если внутри кода есть апостроф, то код надо обрамить двойными апострофами:

``There is a literal backtick (`) here.``

## Горизонтальная черта

Создается тремя звездочками:
***

Или тремя дефисами:

---

## Заключение
