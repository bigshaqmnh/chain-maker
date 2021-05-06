Задача создать объект `chainMaker`, создающий цепь. Финальная цепь это строка вида `( value1 )~~( value2 )~~( value3 )`. У объекта chainMaker должно быть несколько методов для создания и модификации цепи:
- `getLength` - возвращает длину текущей цепи;
- `addValue(value)` - добавляет строку со значением к цепи;
- `removeValue(position)` - удаляет значение по индексу из цепи;
- `reverseChain` - переворачивает цепь;
- `finishChain` - завершает цепь и возвращает ее значение.

Только методы `addValue`, `reverseChain` и `removeValue` вызываются цепочкой, остальные нет.
Если метод `addValue` вызывается без аргументов, то он добавляет пустое значение (пустую строку).
Если метод `removeLink` вызывается с несуществующим индексом или не number значением, нужно выкинуть соотвутствующую ошибку.
После вызова метода `finishChain` существующая цепь должна быть удалена.

Примеры работы:

```chainMaker.addValue(1).addValue(2).addValue(3).finishChain() => '( 1 )~~( 2 )~~( 3 )'```

```chainMaker.addValue(1).addValue(2).removeValue(1).addLink(3).finishChain() => '( 2 )~~( 3 )'```

```chainMaker.addValue(1).addValue(2).reverseChain().addValue(3).finishChain() => '( 2 )~~( 1 )~~( 3 )'```
