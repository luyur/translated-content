---
title: compositionend
slug: Web/API/Element/compositionend_event
---
<p>当文本段落的组成完成或取消时，compositionend 事件将被触发 (具有特殊字符的触发，需要一系列键和其他输入，如语音识别或移动中的字词建议)。</p>

<table class="properties">
 <tbody>
  <tr>
   <td>Bubbles</td>
   <td>Yes</td>
  </tr>
  <tr>
   <td>Cancelable</td>
   <td>Yes</td>
  </tr>
  <tr>
   <td>Target objects</td>
   <td>{{domxref("Element")}}</td>
  </tr>
  <tr>
   <td>Interface</td>
   <td>{{domxref("TouchEvent")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="Properties">Properties</h2>

<table>
 <thead>
  <tr>
   <th scope="col">Property</th>
   <th scope="col">Type</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>target</code> {{ReadOnlyInline}}</td>
   <td>{{domxref("EventTarget")}}</td>
   <td>聚焦元素处理成分</td>
  </tr>
  <tr>
   <td><code>type</code> {{ReadOnlyInline}}</td>
   <td>{{domxref("DOMString")}}</td>
   <td>事件类型</td>
  </tr>
  <tr>
   <td><code>bubbles</code> {{ReadOnlyInline}}</td>
   <td><code>boolean</code></td>
   <td>事件是否冒泡</td>
  </tr>
  <tr>
   <td><code>cancelable</code> {{ReadOnlyInline}}</td>
   <td><code>boolean</code></td>
   <td>是否可以取消该事件</td>
  </tr>
  <tr>
   <td><code>view</code> {{ReadOnlyInline}}</td>
   <td>{{domxref("WindowProxy")}}</td>
   <td>{{domxref("Document.defaultView")}} (<code>window</code> of the document)</td>
  </tr>
  <tr>
   <td><code>detail</code> {{ReadOnlyInline}}</td>
   <td><code>long</code> (<code>float</code>)</td>
   <td>0.</td>
  </tr>
  <tr>
   <td><code>data </code>{{ReadOnlyInline}}</td>
   <td>{{domxref("DOMString")}} (string)</td>
   <td>正在编辑的原始字符串，否则为空字符串。只读。</td>
  </tr>
  <tr>
   <td><code>locale</code></td>
   <td>{{domxref("DOMString")}} (string)</td>
   <td>组合事件的语言代码 (如果可用);否则，为空字符串。只读。</td>
  </tr>
 </tbody>
</table>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.Element.compositionend_event")}}

<h2 id="Related_events">Related events</h2>

<ul>
 <li>{{Event("compositionstart")}}</li>
 <li>{{Event("compositionupdate")}}</li>
</ul>