---
description: >-
  Used to render things, remember these must only be called on paint event too,
  jackass
---

# Render



***

#### render.rectangle

{% code overflow="wrap" lineNumbers="true" %}
```lua
render.rectangle([int] x, [int] y, [int] w, [int] h, [color] col)
```
{% endcode %}

| Argument | Type    | Desc                                      |
| -------- | ------- | ----------------------------------------- |
| x        | integer | horizontal screen position                |
| y        | integer | vertical screen position                  |
| w        | integer | how far right should the rectangle extend |
| h        | integer | how far down should the rectangle extend  |
| col      | color   | what color the rectangle should be        |

***

#### render.filled\_rectangle

{% code overflow="wrap" lineNumbers="true" %}
```lua
render.filled_rectangle([int] x, [int] y, [int] w, [int] h, [color] col)
```
{% endcode %}

| Argument | Type    | Desc                                      |
| -------- | ------- | ----------------------------------------- |
| x        | integer | horizontal screen position                |
| y        | integer | vertical screen position                  |
| w        | integer | how far right should the rectangle extend |
| h        | integer | how far down should the rectangle extend  |
| col      | color   | what color the rectangle should be        |

***

#### render.rounded\_rectangle

{% code overflow="wrap" lineNumbers="true" %}
```lua
render.rounded_rectangle([int] x, [int] y, [int] w, [int] h, [int] points, [int] radius, [color] col)
```
{% endcode %}

| Argument | Type             | Desc                                                   |
| -------- | ---------------- | ------------------------------------------------------ |
| x        | integer          | horizontal screen position                             |
| y        | integer          | vertical screen position                               |
| w        | integer          | how far right should the rectangle extend              |
| h        | integer          | how far down should the rectangle extend               |
| points   | integer          |                                                        |
| radius   | integer (pixels) | how far from the original corner should rounding occur |
| col      | color            | what color the rectangle should be                     |

***

#### render.filled\_rounded\_rectangle

{% code overflow="wrap" lineNumbers="true" %}
```lua
render.filled_rounded_rectangle([int] x, [int] y, [int] w, [int] h, [int] points, [int] radius, [color] col)
```
{% endcode %}

| Argument | Type             | Desc                                                   |
| -------- | ---------------- | ------------------------------------------------------ |
| x        | integer          | horizontal screen position                             |
| y        | integer          | vertical screen position                               |
| w        | integer          | how far right should the rectangle extend              |
| h        | integer          | how far down should the rectangle extend               |
| points   | integer          |                                                        |
| radius   | integer (pixels) | how far from the original corner should rounding occur |
| col      | color            | what color the rectangle should be                     |

***

#### render.line

{% code overflow="wrap" lineNumbers="true" %}
```lua
render.line([int] x, [int] y, [int] x2, [int] y2, [color] col)
```
{% endcode %}

| Argument | Type    | Desc                                       |
| -------- | ------- | ------------------------------------------ |
| x        | integer | the horizontal starting point of your line |
| y        | integer | the vertical starting point of your line   |
| x2       | integer | the horizontal ending point of your line   |
| y2       | integer | the vertical ending point of your line     |
| col      | integer | the color of your line                     |

***
