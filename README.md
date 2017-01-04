Общероссийский классификатор видов экономической деятельности  
(утв. Приказом Росстандарта от 31.01.2014 N 14-ст) (ред. от 26.08.2016)

База данных классификаторов и разделов. 
Данные взяты из базы "КонсультантПлюс" от декабря 2016г

Пакет содержит готовую базу из 2х таблиц, разделы и классификаторы `vendor/carono/okvad2/okvad.sql`, а так же json вариант `vendor/carono/okvad2/data.json`

Для работы с json предоставлен класс: `\carono\okvad\Okvad2`

Список методов:
==============
`Okvad2::getByCode('01.24')` - Заголовок, описание и дополнительные ссылки деятельности  
```
array (size=4)
  'caption' => string 'Выращивание семечковых и косточковых культур' (length=84)
  'notes' => 
    array (size=0)
      empty
  'description' => string 'Эта группировка включает:
  - выращивание таких семечковых и косточковых плодов, как: яблоки, абрикосы, вишня и черешня, 
  персики и нектарины, груши и айва, сливы и терн, прочие семечковые и косточковые плоды' (length=373)
  'section' => string 'A' (length=1)
```  
`Okvad2::getCaptionByCode('01.24') - Заголовок деятельности`  
> Выращивание семечковых и косточковых культур  

`Okvad2::getDescriptionByCode('01.24')` - Описание деятельности
>Эта группировка включает:
>\- выращивание таких семечковых и косточковых плодов, как: яблоки, абрикосы, вишня и черешня, 
>персики и нектарины, груши и айва, сливы и терн, прочие семечковые и косточковые плоды

`Okvad2::getCodesInSection('A')` - Массив кодов  
`Okvad2::getSection('A')` - Раздел с заголовком, описанием и всеми кодами в нём  
`Okvad2::getSections()` - Все разделы со всеми данными    

В массиве с кодами присутствует элемент `notes` - это массив из номеров кодов, которые встречаются в описании.
