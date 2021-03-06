# Преобразование кодировок
[](appencode)

##### Принимаемые элементы:

`replace:` текст, использующийся для замены символов. По умолчанию используется `uFFFD` для символов Unicode и `?` для других символов;

`:invalid => :replace` - замена ошибочных байтов;

`:undef => :replace` - замена отсутствующих символов;

`:fallback => encoding` - изменение кодировки отсутствующих символов;

`:xml => :text` - экранирование символов из XML CharData. Результат может быть использован в HTML 4.0:

+ & на `&amp`;
+ < на `&lt`;
+ > на `&gt`;
+ замена отсутствующих символов на байты вида `&x` (где x - цифра в шестнадцатеричной системе счисления).

`:xml => :attr` - экранирование символов из XML AttrValue. Результат выделяется двойными кавычками и может быть использован для значений свойств в HTML 4.0:

+ & на `&amp`;
+ < на `&lt`;
+ > на `&gt`;
+ `"` на `&quot`;
+ замена отсутствующих символов на байты вида `&x` (где x - цифра в шестнадцатеричной системе счисления).

`cr_newline:` true - символы LF (\n) заменяются на CR (\r);

`crlf_newline:` true - символы LF (\n) заменяются на CRLF (\r\n);

`universal_newline:` true - символы CR (\r) и CRLF (\r\n) заменяются на LF (\n).

*****