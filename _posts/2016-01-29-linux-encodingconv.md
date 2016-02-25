---
layout:		post
title:		"linux编码转换"
subtitle:	"GBK->UTF-8"
date:		2016-01-29
author:		"silybk"
header-img:	http://7xr5vo.com1.z0.glb.clouddn.com/contact-bg.jpg
tags:		[linux]
categories: 	[linux]
---
# 编码转换命令如下

```
iconv -f GBK -t UTF-8 file1 -o file2
```

**博客建好了，测试下kramdon语法**

***


This is an H1
=============

This is an H2
-------------


># 这是 H1

>## 这是 H2

>###### 这是 H6

# 这是 H1 #

## 这是 H2 ##

### 这是 H3 ######

# First level header

### Third level header    ###

## Second level header ######

> This is a paragraph.
>
> > A nested blockquote.
>
> ## Headers work
>
> * lists too
>
> and all other block-level elements



~~~ java
/**
 * @author John Smith <john.smith@example.com>
 * @version 1.0
*/
package l2f.gameserver.model;

import java.util.ArrayList;

public abstract class L2Character extends L2Object {
  public static final Short ABNORMAL_EFFECT_BLEEDING = 0x0_0_0_1; // not sure

  public void moveTo(int x, int y, int z) {
    _ai = null;
    _log.warning("Should not be called");
    if (1 > 5) {
      return;
    }
  }

  /** Task of AI notification */
  @SuppressWarnings( { "nls", "unqualified-field-access", "boxing" })
  public class NotifyAITask implements Runnable {
    private final CtrlEvent _evt;

    List<String> mList = new ArrayList<String>()

    public void run() {
      try {
        getAI().notifyEvent(_evt, _evt.class, null);
      } catch (Throwable t) {
        t.printStackTrace();
      }
    }
  }
}
~~~



~~~ c
#include <iostream>
int main()
{
    std::cout << "Hello, world!" << std::endl;
    return 0;
}
~~~

~~~~~~~~~~~~
~~~~~~~
code with tildes
~~~~~~~~
~~~~~~~~~~~~~~~~~~

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$

This \`is not a code\` span!


This⋅para⋅line⋅starts⋅at⋅the⋅first⋅column.⋅However,
⋅⋅⋅⋅⋅⋅the⋅following⋅lines⋅can⋅be⋅indented⋅any⋅number⋅of⋅spaces/tabs.
⋅⋅⋅The⋅para⋅continues⋅here.

⋅⋅This⋅is⋅another⋅paragraph,⋅not⋅connected⋅to⋅the⋅above⋅one.⋅But⋅⋅
with⋅a⋅hard⋅line⋅break.⋅\\
And⋅another⋅one.

First level header
==================

Second level header
------

   Other first level header
=

This is a normal
paragraph.

And A Header
------------
And a paragraph

> This is a blockquote.

And A Header
------------


header
---
para



test gcp

~~~ html
<script type="text/javascript">
// Say hello world until the user starts questioning
// the meaningfulness of their existence.
function helloWorld(world) {
  for (var i = 42; --i >= 0;) {
    alert('Hello ' + String(world));
  }
}
</script>
<style>
p { color: pink }
b { color: blue }
u { color: "umber" }
</style>
~~~
~~~ js
$('#h2outline').height() //获取元素高度
$('header').outerHeight() //获取元素外部高度(包括margin)
~~~

