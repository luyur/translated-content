---
title: Node.isSameNode
slug: Web/API/Node/isSameNode
---
<p>{{ ApiRef() }}</p>

<h2 id="概述">概述</h2>
<p>判断两个节点是否是相同的节点，即指向同一个对象。</p>
<div class="warning">
 <strong>警告：</strong>该方法已在 DOM level 4 中被废弃，最近的浏览器版本 (Gecko 10.0 {{ geckoRelease("10.0") }}.) 已经删除了这个方法。也就是说，不要再使用 <code>node1.isSameNode(node2)</code> 而使用 <code>node1 === node2</code> 或者 <code>node1 == node2</code> 来代替。</div>
<h2 id="语法">语法</h2>
<pre class="eval">var <em>isSameNode</em> = <em>node</em>.isSameNode(<em>other</em>);
</pre>
<ul>
 <li><code>other</code>是要和<code>node</code>判断相同性的另一个节点。</li>
</ul>
<h2 id="规范">规范</h2>
<ul>
 <li><a href="http://www.w3.org/TR/DOM-Level-3-Core/core.html#Node3-isSameNode">DOM Level 3 Core: isSameNode</a></li>
 <li>This has been removed from <a href="http://www.w3.org/TR/domcore/">DOM Core Level 4</a></li>
</ul>