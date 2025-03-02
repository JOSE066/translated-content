---
title: Node.compareDocumentPosition
slug: Web/API/Node/compareDocumentPosition
translation_of: Web/API/Node/compareDocumentPosition
---

{{ ApiRef() }}

## Аннотация

Сравнивает позицию текущего узла и другого узла в любом другом документе.

## Синтаксис

```
node.compareDocumentPosition( otherNode )
```

- `node` это узел, который сравнивается
- `otherNode` это узел, с которым идёт сравнение.

Возвращаемое значение вычисляется как отношение, которое имеется между `otherNode` и `node`.

## Примечание

Возвращаемое значение - это битовая маска со следующими значениями:

| Имя                                         | Значение |
| ------------------------------------------- | -------- |
| `DOCUMENT_POSITION_DISCONNECTED`            | 1        |
| `DOCUMENT_POSITION_PRECEDING`               | 2        |
| `DOCUMENT_POSITION_FOLLOWING`               | 4        |
| `DOCUMENT_POSITION_CONTAINS`                | 8        |
| `DOCUMENT_POSITION_CONTAINED_BY`            | 16       |
| `DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC` | 32       |

## Пример

```js
var head = document.getElementsByTagName('head').item(0);
if (head.compareDocumentPosition(document.body) & Node.DOCUMENT_POSITION_FOLLOWING) {
  console.log("well-formed document");
} else {
  console.log("<head> is not before <body>");
}
```

> **Примечание:** **Замечание:** _Из-за того, что результат, возвращаемый_ `compareDocumentPosition`, является битовой маской, [побитовый оператор и](/ru/docs/JavaScript/Reference/Operators/Bitwise_Operators) должен использоваться для осмысленных значений.

## Спецификации

| Спецификация                                                                                 | Статус         | Комментарий |
| -------------------------------------------------------------------------------------------- | -------------- | ----------- |
| [DOM Level 3](http://www.w3.org/TR/DOM-Level-3-Core/core.html#Node3-compareDocumentPosition) | Рекомендация   |             |
| [DOM Standard](http://dom.spec.whatwg.org/#dom-node-comparedocumentposition)                 | Живой стандарт |             |

## Смотрите также

- [`Node.contains`](/en-US/docs/DOM/Node.contains)
- [John Resig - Comparing Document Position](http://ejohn.org/blog/comparing-document-position/)
