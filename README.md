# Сайт-проект "Научиться учиться".

## Данный сайт-проект уделяет внимание теме современных и эффективных подходов в обучении.
------
Функциональность проекта заключается в том, что страница поделена на несколько секций, которые предоставляют различные информационные блоки с рекомендациями и фактами о современных подходах в обучении. Полученные знания человек может использовать в своей жизни и повысить эффективность своего самообразования.

Проект содержит информационные карточки с изображениями, также блоки с видеомодулями. Но помимо этого имеет ссылки для приобретения тематической литературы, а также ссылки на различные статьи связанные с темой обучения. В конце страницы предоставлен блок со ссылками на полезные ресурсы, а также блок с навигацией, где имеется возможность перейти на социальные сети проекта или ознакомиться с концепциями и наставниками.

Проект написан в ходе образовательной работы на [Яндекс Практикуме](https://practicum.yandex.ru/).

## В проекте используются различные технологии.
------
 Самое первое, что основан на файловой структуре *БЭМ-Nested* методологии. Из интересных приёмов, в проекте использованы блоки анимации на технологии CSS 'keyframes'
 ```css
 @keyframes rotation_elements {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}

.rotation {
  animation: rotation_elements 20s linear infinite;
}
```
  и 'transitions', чтобы сделать элементы страницы более интерактивными.

 ```css
.transition {
  transition: opacity .7s ease;
}

.transition:hover {
  opacity: .4;
}
 ```

В большинстве блоков страницы проекта используется технология 'Flexbox', для более удобного расположения элементов.

 ```css
.cards {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  gap: 0px 100px;
}
  ```

Технология CSS 'Position' позволяет разместить в сетке страницы изображения в нужных местах, для того, чтобы проект соотвествовал предоставленному брифу.

```css
.feynman__image {
  position: absolute;
  left: 0;
  bottom: 0;
```

Одна из технологии 'Z-Index' дает возможность размещать элементы в глубину, что решает проблему наложения изображений на текст при масштабирования страницы, теперь всегда текст отображается поверх элементов изображений и различных декоративных фигур на странице.

```css
.feynman__image {
  z-index: -1;
}
```

## Планы по доработке проекта
------
1. Также будет необходимо проверить код на кроссбраузерность и дописать все вендорные префиксы.
2. В планах по доработке проекта сделать дизайн формы обратной связи, чтобы пользователь мог оставить свой комментарий о данной странице об обучении.
