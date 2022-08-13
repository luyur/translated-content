---
title: Селекторы по ID
slug: Web/CSS/ID_selectors
translation_of: Web/CSS/ID_selectors
---
<div>{{ CSSRef() }}</div>

<h2 id="Summary">Краткое описание</h2>

<p>В HTML-документах CSS-селекторы по ID производят выборку всех элементов по ID, полностью совпадающих с селектором.</p>

<h2 id="Syntax">Синтаксис</h2>

<pre class="syntaxbox">#id_value { <em>style properties</em> }</pre>

<p>То же самое  — {{ Cssxref("Attribute_selectors", "селектор по атрибутам") }}:</p>

<pre class="syntaxbox">[id=id_value] { <em>style properties</em> }</pre>

<h2 id="Example">Пример</h2>

<pre class="brush: css">span#identified {
  background-color: DodgerBlue;
}
</pre>

<pre class="brush: html">&lt;span id="identified"&gt;Тут span с каким-то текстом.&lt;/span&gt;
&lt;span&gt;Здесь тоже span.&lt;/span&gt;
</pre>

<p>{{ EmbedLiveSample('Example', 200, 50) }}</p>

<h2 id="Specifications">Спецификации</h2>

{{Specifications}}

<h2 id="Поддержка_браузерами">Поддержка браузерами</h2>

<p>{{Compat}}</p>