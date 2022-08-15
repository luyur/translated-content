---
title: Range.endOffset
slug: Web/API/Range/endOffset
---
<div>{{ApiRef("DOM")}}</div>

<p>只读属性 <code><strong>Range.endOffset</strong></code> 返回代表 <code style="font-style: normal; line-height: 1.5;">Range</code> 结束位置在 {{domxref("Range.endContainer")}} 中的偏移值的数字。</p>

<p>如果 <code>endContainer</code> 的 {{domxref("Node")}} 类型为 {{domxref("Text")}}, {{domxref("Comment")}}，或 {{domxref("CDATASection")}}，偏移值是 <code>endContainer</code> 节点开头到 {{domxref("Range")}} 末尾的总字符个数。对其他类型的 {{domxref("Node")}} ， <code>endOffset</code> 指 <code>endContainer</code> 开头到 {{domxref("Range")}} 末尾的总 {{domxref("Node")}} 个数。如需修改 <code>endOffset</code> 的值， 使用 {{domxref("Range.setEnd")}} 方法。</p>

<h2 id="Syntax">语法</h2>

<pre class="syntaxbox"><em>endRangeOffset</em> = <em>range</em>.endOffset;
</pre>

<h2 id="Example">示例</h2>

<pre class="brush:js">var range = document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
endRangeOffset = range.endOffset;</pre>

<h2 id="Specification">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat("api.Range.endOffset")}}</p>

<h2 id="参见">参见</h2>

<ul>
 <li><a href="/en-US/docs/DOM/DOM_Reference">The DOM interfaces index</a></li>
</ul>