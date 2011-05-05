---
layout: default
title: Статьи
id: articles
---

Статьи
======

Здесь будут собираться русскоязычные и не очень статьи по Sinatre. 
Переводные, либо оригинальные.

### [Hello world с помощью Ruby, Sinatra и Haml](http://justlest.info/2010/01/hello-world-ruby-sinatra-haml )

Совсем небольшая статья, ничего сложного.

### [Запуск web-приложения на Sinatra с Phusion Passenger](http://justlest.info/2010/01/run-sinatra-passenger)


Пример развёртывания Sinatra приложения с помощью Passager. По сути пример развёртывания Rack приложения (файловая структура).

### [Sinatra и DataMapper: пример сервиса сокращения ссылок](http://justlest.info/2010/02/sinatra-datamapper-url-shortener)

Хорошая статья по созданию приложения работающего с Базой Данных (DataMapper). Пример создания "хелпера".
Работающее приложение размещено на Heroku по адресу [http://tourl.heroku.com](http://tourl.heroku.com/)


### Домашний файлообменник на базе Sinatra и DataMapper

Серия публикаций на habrahabr, достаточно информационно.

 * [Часть 1 -- The Begining](http://habrahabr.ru/blogs/ruby/50031/)
 * [Часть 2 -- Advanced features](http://habrahabr.ru/blogs/ruby/50084/)
 * [Часть 3 -- Very Advanced features](http://habrahabr.ru/blogs/ruby/50348/ )

### [Отправка писем из проектов на Sinatra](http://blog.copperred.net/2009/09/sending-mail-from-sinatra/)

Использование библиотечки Pony, для отправки почты. Отмечу, что "post '/doemail/' do
означает, что должна быть форма с которой уже приходит запрос в Синатру - POST метод.
Так же "erb(:contact_form)" означает, что для тела сообщения "отрисовывается" шаблон 
с названием "contact_form", это должен быть файл contact_form.html.erb в папке шаблонов отображения "views".
При этом шаблон формата Erb - то есть EmbeddedRuby.


### [Фильтрация rss-потоков с помощью Sinatra и HTTParty](http://lonelyelk.ru/posts/10)

Подключение своей библиотеки обработки rss потоков, и отображение результата с помощью Синатры.


### [A contact form for Jekyll, powered by Sinatra ](http://vitobotta.com/sinatra-contact-form-jekyll/)

Добавление формы обратной связи для Jekyll сгенерированного сайта.


### [20+ Rubyists are using Sinatra – Do you?](http://rubylearning.com/blog/2009/06/29/20-rubyists-using-sinatra-do-you/)

Отзывы пользователей Синатры. Английский.

### [Clone TinyURL in 40 lines of Ruby code](http://blog.saush.com/2009/04/13/clone-tinyurl-in-40-lines-of-ruby-code/)

Очередной клон TinyURL, код приложения размещён [здесь](http://github.com/sausheong/snip/), встроенный шаблон отображения.
Приведён пример загрузки на Heroku.

### [Sinatra Cookbook project](http://ididitmyway.heroku.com/)

Очень хороший блог с публикацями по Синатре, надо будет попереводить :)