# jQuery FormStyler Modern <sup>[2.x](https://github.com/ange007/JQueryFormStylerModern/blob/dev/CHANGELOG.md)</sup> 
[![Latest Stable Version](https://poser.pugx.org/ange007/jquery-formstyler-modern/v/stable)](https://packagist.org/packages/ange007/jquery-formstyler-modern)
[![Total Downloads](https://poser.pugx.org/ange007/jquery-formstyler-modern/downloads)](https://packagist.org/packages/ange007/jquery-formstyler-modern)
[![License](https://poser.pugx.org/ange007/jquery-formstyler-modern/license)](https://packagist.org/packages/ange007/jquery-formstyler-modern)
[![Build Status](https://travis-ci.org/ange007/JQueryFormStyler-Modern.svg?branch=dev)](https://travis-ci.org/ange007/JQueryFormStyler-Modern)

> Самостоятельное ответвление от плагина **[jQueryFormStyler](https://github.com/Dimox/jQueryFormStyler)** 

- [Demo](http://ange007.github.io/JQueryFormStyler-Modern/)
- [Changelog](https://github.com/ange007/JQueryFormStylerModern/blob/dev/CHANGELOG.md)
- [Download](https://github.com/ange007/JQueryFormStyler-Modern/releases)

## Info
JQuery HTML form styling plugin:
- `<input type="checkbox">`
- `<input type="radio">`
- `<input type="file">`
- `<input type="number">`
- `<input type="password">`
- `<select>`

## Attention!
Settings from plugin vesion **2.x** - differ from version **1.x**.
> Структура настроек плагина версии **2.x** - отличаются от настроек [оригинального](https://github.com/Dimox/jQueryFormStyler) и версии [1.x](https://github.com/ange007/JQueryFormStyler-Modern/tree/1.x---release) данного плагина.

## Install
Composer:
```sh
$ php composer.phar require "ange007/jquery-formstyler-modern"
```
Bower:
```sh
$ bower install --save-dev ange007/jquery-formstyler-modern
```

## Getting Started
Main plugin file - `jquery.formStylerModern.js`.
Connection of styles is possible in two ways:
- `jquery.formStylerModern.css` *(frame and default style)*
- Frame file - `/style/jquery.formStylerModern.frame.css` and style file - `/style/jquery.formStylerModern.(default|flat|etc).css`

> Сам плагин подключается посредством файла `jquery.formStylerModern.js`.
> Подключение стилей возможно в 2х вариантах:
> - Подключение `jquery.formStylerModern.css` - который в себе содержит каркас и тему по умолчанию *(default)*
> - Подключение файлов из директории `/style/` - `jquery.formStylerModern.frame.css` *(каркас)* и одной из тем в той-же директории *(например `jquery.formStylerModern.flat.css`)*

## Works
Stylish elements. `/ Стилизация элементов.`
```javascript
$( 'input, select, button' ).styler( 
{
	locale: 'ru',
	select: { 
		search: {
			limit: 10
		}
	},
	onFormStyled: function( ) 
	{ 
		...
	}
} );
```


Reload plugin with certain settings. `/ Перезагрузка элементов с определёнными настройками.`
```javascript
$( '#checkbox-indeterminate-change' ).styler( 'reinitialize', { checkbox: { indeterminate: true } } );
```


Clean style. `/ Убрать стилизацию.`
```javascript
$( 'input, select, button' ).styler( 'destroy' );
```


Repaint after "manual" change. `/ Перерисовка компонента после "ручного" изменения состояния.`
```javascript
$( this ).prop( 'disabled', true )
	.trigger( 'repaint' );
```