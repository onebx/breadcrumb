# breadcrumb
### Навигационная цепочка
Настройки этого компонента позволяют регулировать уровень вложенности разделов (корень сайта - ноль), начиная с которого начнет выводиться навигационная цепочка. Также возможно переопределить путь, для которого цепочка будет построена и т.д.

## Пример вызова
```php
<?php
$APPLICATION->IncludeComponent(
  'bitrix:breadcrumb',
  '',
  [
    'START_FROM' => '0', 
    'PATH' => '', 
    'SITE_ID' => 's1' 
  ]
);?>
```

## Параметры
Поле | Параметр | Описание
--- | --- | ---
Номер пункта, начиная с которого будет построена навигационная цепочка | START_FROM | Указывается номер пункта, начиная с которого будет построена навигационная цепочка. В поле может быть задано числовое значение, определяющее уровень вложенности раздела на сайте. <br> Например, 0 (ноль) означает, что построение навигационной цепочки начнется от корня сайта. Если 1, то с первого уровня текущего раздела и так далее.
Путь, для которого будет построена навигационная цепочка (по умолчанию, текущий путь) | PATH | Указывается путь, по которому будет построена навигационная цепочка. Если поле не заполнено совсем, то навигационная цепочка будет строиться для текущего пути.
Cайт (устанавливается в случае многосайтовой версии, когда DOCUMENT_ROOT у сайтов разный) | SITE_ID | Указывается сайт для построения навигационной цепочки. Параметр устанавливается в случае многосайтовой версии, когда DOCUMENT_ROOT у сайтов разный.
