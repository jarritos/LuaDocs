---
description: yada yada yada
---

# Utils

***

#### utils.trace\_bullet

{% code overflow="wrap" lineNumbers="true" %}
```lua
utils.trace_bullet([player] shooter, [player] target, [bool] taser, [vector] start, [vector] end, [bool] penetrate): [table]
```
{% endcode %}

| Arguments | Type   | Desc                               |
| --------- | ------ | ---------------------------------- |
| shooter   | player | who should be firing this shot     |
| target    | player | who should be receiving this shot  |
| is\_taser | bool   | is this coming from a taser?       |
| start     | vector | origin of the shot                 |
| end       | vector | resting place of the shot          |
| penetrate | bool   | should the bullet penetrate walls? |

returns penetration\_data\_t

***

#### utils.trace\_line

{% code overflow="wrap" lineNumbers="true" %}
```lua
trace_line([vector] start, [vector] end, [int] mask, [int] trace_type, [player] skip): [table]
```
{% endcode %}

| Arguments   | Type   | Desc                            |
| ----------- | ------ | ------------------------------- |
| start       | vector | beginning point of the line     |
| end         | vector | ending point of the line        |
| mask        | int    |                                 |
| trace\_type | int    | optional.                       |
| skip        | player | optional. skips player provided |

returns trace\_t

***
