Sass Boilerplate for generic CSS/HTML
=============

I'm using this as a starting template for almost any project now.
It includes sprites, assorted mixins (aka code snippets), file structure, jquery+cycle+scrollto (most usable these days).
And, that's it.

You need to have Compass installed for it to work properly.

Structure
=============
`/sass/lib/base` - all the mixins and libs needed for us.

`/sass/screen.sass` - agregates all .sass files.

`/sass/common.sass` - fonts, variables, common blocks, headings, header, footer style.

`/sass/main.sass` - styles for the mainpage.

Naming blocks
=============
I use BEM naming, meaning `.block` for independent block. `.block__element` for elements inside that block. And `.block_modification` for modification of the block.

`layouts.sass` consists of all the columns-header-footer stuff, all with `.l-*` prefixes. So you know its layout.

States of the blocks use prefix `.is-*`. For example `.is-running`, `.is-hidden`, `.is-open`.

Hooks for js should use prefix `.js-*`.

Html codestyle
=============
1) `<title>name page</title>`
2) comments all `layouts` and sufficiently large independent `block`. Comments are separated empty string. Some [example link]http://take.ms/HVqrC

Sass codestyle
=============
// 1) каждый новый блок (не элемент, а блок) имеет такую форму комментариев.
1) Each new block (not element and block) has the form of comments [example link]http://take.ms/hgpNo.
// 2) все элементы блока, должны иметь как минимум одну вложеность (но не боле 3-х) в своего родителя.
2) all the elements of the block must have at least one nested. Some: [example link]http://take.ms/EGuEb.
3) Структура. По умолчанию структура sass такая:
	3.1) common.sass:
		шрифты, 
		переменные, миксины (под текущий проект), экстенды. 
		Общие блоки (body, out, wrap etc), 
		заголовки,
		разное,
		навигация,
		хедер,
		футер,
		3.2) main.sass:
			блоки внутренних страниц
Если проект средний или большой, отдельные елементы, группы елементов, большие блоки могут выносить в отдельный файл. Например кнопки в файл - btn.sass, элементы форм - form.sass, иконки - icons.sass итд

