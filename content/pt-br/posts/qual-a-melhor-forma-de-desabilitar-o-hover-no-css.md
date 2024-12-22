---
layout: default
title: Interaction Media Features
tags:
  - css
date: 2022-03-26T13:01:42.745Z
---
A pseudo-classe `:hover` do CSS define os estilos que um elemento deve apresentar no momento em que o usuário passa o ponteiro do mouse sobre ele.

```css
a {
  color: black;
}

a:hover {
  color: red;
}
```

Em dispositivos mobile, quando tocamos em um elemento interativo (como link ou botão) ele aciona o estado de "hover". Esse estado é mantido até que outro elemento da página seja tocado.

Uma solução bem comum para resolver esse problema é a seguinte:

```css
a {
  color: black;
}

@media (min-width: 1170px) {
  a:hover {
    color: red;
  }
}
```

Mas essa é a melhor solução? Vamos considerar as seguintes situações:

1. O usuário tem um monitor grande e reduziu o tamanho da janela do navegador.

2. O usuário está em um computador, mas não usa um mouse para navegar.

Para considerar esses pontos podemos usar outro tipo de media query:

```css
a {
  color: black;
}

@media (hover: hover) and (pointer: fine) {
  a:hover {
    color: red;
  }
}
```

Isso é uma adição a especificação de Media Queries e são chamadas de [“Interaction Media Features”](https://drafts.csswg.org/mediaqueries-4/#mf-interaction).