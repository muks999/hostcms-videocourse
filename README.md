# Видеокурс «Создать интернет-магазин на Hostcms за 4 часа»
Сам видеокурс находится здесь: [Видеокурс на Youtube](https://www.youtube.com/playlist?list=PLkuR2FZXP-9nsW0AX4b-RO8qF3B5D4gC6)
Здесь же будет краткая инструкция, ответы на вопросы, файлы к видео и html-шаблон.

## Инструкция
1. [скачайте html-шаблон](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/eshopper.zip)
2. [установите систему](https://www.youtube.com/watch?v=UrMPCQFWWVE&list=PLkuR2FZXP-9nsW0AX4b-RO8qF3B5D4gC6&index=3)
3. Смотрите все видео и пробуйте самостоятельно

## Файлы и коды из видео

### Для 5 урока

Для автоматических метатегов:
```php
<meta charset="<?php echo SITE_CODING?>">
<title><?php Core_Page::instance()->showTitle()?></title>
<meta name="description" content="<?php Core_Page::instance()->showDescription()?>">
<meta name="keywords" content="<?php Core_Page::instance()->showKeywords()?>">
<meta name="author" content="Ваше имя">
```

### Для 11 урока

[Код краткой корзины](http://nikolaigromkov.ru/all/vidzhet-kratkoy-korziny/). [Файл XSL-шаблона «МагазинКорзинаКраткая»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/11_МагазинКорзинаКраткая.txt).
И в макет вставить:

```php
<? php $this->showSection('ИМЯ_ВИДЖЕТА'); ?>
```
### Для 12 урока

[Файл XSL-шаблона «КорзинаКраткаяНовая»](12_КорзинаКраткаяНовая.txt)

[Код краткой корзины](http://nikolaigromkov.ru/all/ajax-cart/)
Меняйте ссылки добавления в корзину в XSL-шаблонах «МагазинКаталогТоваров» и «МагазинТовар»
В списке товаров ссылку на добавление можно найти по участку кода
<xsl:if test="type = 0 or (type = 1 and (digitals > 0 or digitals = -1)) or type = 2">
</xsl:if>
или поиском по AddIntoCart

### Для 14 урока

[Файл XSL-шаблона «МагазинКаталогТоваровНовый»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/14_МагазинКаталогТоваровНовый.txt).

### Для 15 урока

[Вывод дополнительных свойств в XSL](http://nikolaigromkov.ru/all/shpargalka-po-hostcms-xsl/)
```xsl
<xsl:value-of select="property_value[tag_name='email']/value"/>
<a href="{dir}{property_value[tag_name='file']/file}" target="_blank">Скачать <xsl:value-of select="property_value[tag_name='file']/file_name"/></a>
<a href="{dir}{property_value[tag_name='file']/file}" target="_blank"><img src="{dir}{property_value[tag_name='file']/file_small}" /></a>
```

### Для 16 урока

[Файл виджета «ВИДЖЕТ_ТОВАРОВ_ПО_ГРУППЕ»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/16_ВИДЖЕТ_ТОВАРОВ_ПО_ГРУППЕ.txt).

### Для 17 урока

[Файл XSL-шаблона «МагазинКаталогТоваровВкладки»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/17_МагазинКаталогТоваровВкладки.txt).

### Для 19 урока

[Файл с кодом «ВыводТоваровПоФлажку»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/19_ВыводТоваровПоФлажку.txt).

Вот к тому же ссылка: http://nikolaigromkov.ru/all/vyvod-tovarov-po-flazhku/

### Для 20 урока

[Файл виджета «ВиджетВыводаТоваровПоФлажку»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/20_ВиджетВыводаТоваровПоФлажку.txt).

### Для 21 урока

[Файл XSL-шаблона «РекомендуемыеXSL»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/21_РекомендуемыеXSL.txt).

[Дополнительная ссылка из видео](http://nikolaigromkov.ru/all/razdelenie-po-blokam/)

### Для 23 урока

Вот код вывода бейджиков, предварительно настройте дополнительные свойства:
```xsl
<xsl:choose>
	<xsl:when test="property_value[tag_name='sale']/value != 0">
		<img src="/source/images/home/sale.png" class="new" alt="" />
	</xsl:when>
	<xsl:when test="property_value[tag_name='new']/value != 0">
		<img src="/source/images/home/new.png" class="new" alt="" />
	</xsl:when>
</xsl:choose>
```

### Для 24 урока

[Шрифт рубля](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/ptrouble.zip)

### Для 25 урока

[Файл XSL-шаблона «СписокПроизводителей»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/25_СписокПроизводителей.txt).

### Для 26 урока

[Код вывода групп товаров](http://nikolaigromkov.ru/all/gruppy-tovarov/)

### Для 21 урока

[Файл XSL-шаблона «МагазинФильтр»](https://github.com/NivaksStudio/hostcms-videocourse/blob/master/29_МагазинФильтр.txt).
[Скрипт для отслеживания ползунка здесь](http://nikolaigromkov.ru/all/stilizaciya-filtra/)
