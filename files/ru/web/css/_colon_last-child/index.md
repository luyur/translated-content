---
title: ':last-child'
slug: 'Web/CSS/:last-child'
translation_of: 'Web/CSS/:last-child'
---
<div>{{CSSRef}}</div>

<h2 id="Описание">Описание</h2>

<p>CSS <a href="/ru/docs/Web/CSS/Pseudo-classes">псевдокласс</a> <code>:last-child</code> находит любой элемент, являющийся последним в его родителе.</p>

<h2 id="Синтаксис">Синтаксис</h2>

<pre class="syntaxbox">element:last-child { <em>style properties</em> }</pre>

<h2 id="Пример">Пример</h2>

<h3 id="HTML">HTML</h3>

<pre class="brush: html">&lt;ul&gt;
  &lt;li&gt;Этот элемент не лаймовый.&lt;/li&gt;
  &lt;li&gt;И этот тоже.&lt;/li&gt;
  &lt;li&gt;А этот да! :)&lt;/li&gt;
&lt;/ul&gt;</pre>

<h3 id="CSS">CSS</h3>

<pre class="brush: css">li:last-child {
  background-color: lime;
}</pre>

<p>{{EmbedLiveSample('Пример', '100%', 100)}}</p>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Поддержка_браузерами">Поддержка браузерами</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li>{{cssxref(":first-child")}}</li>
 <li>{{cssxref(":nth-child")}}</li>
 <li>{{cssxref(":last-of-type")}}</li>
</ul>