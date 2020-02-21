---
description: Columns and Rows
---

# Grid Layout

### Designing with a Grid

Every good web design begins with a sketch. As you may have noticed, everything in CSS has to be mathematically laid out. You need to have dimensions for your margins, padding, etc. This requires that these sketches are built with a "grid" in mind to help with alignments. 

![](https://lh6.googleusercontent.com/4jiCQAaxNGHURFWaTtevTNWQo3Iq3QPVLaDSt_ygloHhRnDRPSHDO_DZh8z_STbmmrg7aSHsrw61AmALuiNHjPCDXoUefj8u0-T2qIzCt66Kk67AdtsZ4vcZbJTWx1eXkRwt2fVuSI8)

Because every aspect of a site’s “look” is defined by HTML/CSS – it is crucial to have a detailed sketch going in.

Pay particular attention to the location of navigation bars, titles, headers, content, images, footers etc. 

When imagining alignments, in particular, be mindful of the **grid**.

#### Rows and Columns

The grid is made up of rows and columns. Columns run from left to right accross the width of the page. \(The green bars in the above picture\). Rows run horizontally from top to bottom.

It's important to break down websites into rows and columns.

![](../../../.gitbook/assets/image%20%287%29.png)

How many rows and columns do you see?

{% tabs %}
{% tab title="Rows" %}


![](https://lh3.googleusercontent.com/hrUy4iXPzjqmRZJEJkaiXkUEbO03Wye_ra4SNK8drh4yOVFr9U3rgiXZDq1pJVtg5jS0-41QuuRd0LSZnd8iKsOcZ_4ftXvqoIPk9m2LfxVZmX_RzQs65xOSparlWsThRQv5nsBF6TY)
{% endtab %}

{% tab title="Columns" %}
![](https://lh4.googleusercontent.com/w6aRkar42IC4455uvRppWqmOfeiXltAaqG_-xcizR9VVw9mPJ9vjMFtBquQOpKjaBQZdQydpLmzQykuCkrrEziPKCZsBJy0_cjSD7t1oVuhqVQ1yizLEZ6XyJrWQTe3mFRWdB30xF-w)
{% endtab %}
{% endtabs %}

In this example, the footer is included as a row, but not the header. This is a rather arbitrary choice, but partially based on the fact that navbars aren't a part of the bootstrap grid system. We will get into that more in a moment.



![](https://lh3.googleusercontent.com/2VmFlhJ9-mH07B2rEuvBMFM_sUAIzgHokTjO0XxJ1UnfcTwwY9GmXLPM4Ox8MsPao0UGDJpzkErr1xpPED-XKF_lely33n_1-Mkkt3T9RK0429sG7D6RcPE_4fh-E2HVOXD8NTKXSLQ)

How many rows and columns in this example?

{% tabs %}
{% tab title="Rows" %}
![](https://lh5.googleusercontent.com/ICSvj433VoIXkqaOKrbTub2KDzALyzBUewOR7OyWGe88REvM3bjfnwoelS0uw_X9GE1_eORlxV1SFHozzku3SIadfg0JmBK6BH4U7ttGyPYRtofJLmGMeD9vPeyalTjsh9dDghNqrRU)

\*\*\*You may notice that we lumped together the images and text into a single row. It makes sense to do this when the images and text are essentially "tied" to one another.
{% endtab %}

{% tab title="Columns" %}
![](https://lh5.googleusercontent.com/Js5WJZS0YIGY9jhgRGsfEo8ssg68KNXu4psNoBQHua47Sr7SWFiHaezxIJtbL9P7uVetveh4K-BD2rY0P5lNs6e33GLoQnw13mVvSACkef5gJ7np4RUYy2IHexTJ5lUlFiIponROF6k)
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Notice** that each wireframe represents a different kind of website \(one is a blog, one is a corporate site, etc.
{% endhint %}

#### Sub-rows and Sub-Columns

![](https://lh5.googleusercontent.com/glL5fRZi-VqW-n_sbONcZLxEqprbzJ-YWC47huxMjUzs1XJqFoR5CgC4F_ECIZmnXjoinuFEXoMTSDlcmXQxs6aoILEEpJRT7xxFMONuDrtPkuZE_fUVLvjhklGvDchpsjWtlvZvkQY)

How many rows and columns are in this example?

{% tabs %}
{% tab title="Rows" %}
Larger Rows:

![](https://lh3.googleusercontent.com/gr_gBd4IS764uBl-TN4pe1uLnJhL8dxq2mobLN3jYE13sUtvjT5WKxUdIWwyHGrq55etFyl6PTZIuZ75PMdJAye9dn8oAcC2kTBDCod3lcu2mMJkm6ud_Gjm97zl4tOiIhtTLXpfcqI)

Sub-Rows:

![](https://lh6.googleusercontent.com/SaWqPXAr5LkkuD4Fd0jNpvvjXdoerSJ_vw8KGRIZN2za91t3JeQ3VqFqAxqA4GFNfX1FHCb8B6cDEPoy5ii8azsLQ1gJcbtbACycmbDK8CNbQk4_nTbiT2RgCOFKqTKA53ACLHdJvbs)
{% endtab %}

{% tab title="Columns" %}
Larger Columns:

![](https://lh6.googleusercontent.com/iZzN9_zAbV7uVOUkeFlubmCbySbSJFf7EhI8pgUaKhomH_7RwY_EVf4ngFU9GtaMnkZ9rRCQlXogzS3xHViEh1iE6QRpt_A8qP-FjaHKlHXvE7clzrXph2rnSZ18IyBf9RM8ZtLARLY)

Sub-columns:

![](https://lh3.googleusercontent.com/rmRVHktzfqMLFbn_sNlXhwP3Fc7shJmPFsJCB_WfYF3aaTH869suobULaRQMh_ex2xUScMOgZMspBTPHJceKXAij1Vbqh1_G0jW923vwZrsqpBfcKCSaD8UmKEJm4fbjE6fX2y-lWbU)
{% endtab %}
{% endtabs %}

The way to access sub-elements is to put rows inside columns that are inside of larger rows. Don't worry, this one was tricky! Just remember the big takeaway: webpage layouts can always be broken down into rows and columns.

{% hint style="info" %}
Here are a few wireframing resources:

* [https://balsamiq.com/](https://balsamiq.com/)
* [http://framebox.org/](http://framebox.org/)

There are many tools for wireframes. Balsamiq and Framebox are among the best.
{% endhint %}

