---
title: CanvasRenderingContext2D.lineTo()
slug: Web/API/CanvasRenderingContext2D/lineTo
---
<div>{{APIRef}}</div>

<p><strong><code>CanvasRenderingContext2D.lineTo()</code></strong> 是 Canvas 2D API 使用直线连接子路径的终点到 x，y 坐标的方法（并不会真正地绘制）。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">void <var><em>ctx</em>.lineTo(x, y);</var>
</pre>

<h3 id="参数">参数</h3>

<dl>
 <dt><code>x</code></dt>
 <dd>直线终点的 x 轴坐标。</dd>
 <dt><code>y</code></dt>
 <dd>直线终点的 y 轴坐标。</dd>
</dl>

<h2 id="示例">示例</h2>

<h3 id="使用_lineTo_方法">使用 <code>lineTo</code> 方法</h3>

<p>这是一段使用 <code>lineTo</code> 方法的简单的代码片段。 使用 {{domxref("CanvasRenderingContext2D.beginPath", "beginPath()")}} 绘制路径的起始点，使用 {{domxref("CanvasRenderingContext.moveTo", "moveTo()")}}移动画笔，使用 {{domxref("CanvasRenderingContext2D.stroke", "stroke()")}} 方法真正地画线。</p>

<h4 id="HTML">HTML</h4>

<pre class="brush: html">&lt;canvas id="canvas"&gt;&lt;/canvas&gt;
</pre>

<h4 id="JavaScript">JavaScript</h4>

<pre class="brush: js; highlight:[6]">var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");

ctx.beginPath();
ctx.moveTo(0,0);
ctx.lineTo(100, 100);
ctx.stroke();
</pre>

<p>修改下面的代码并在线查看 canvas 的变化：</p>

<div class="hidden">
<h6 id="Playable_code">Playable code</h6>

<pre class="brush: html">&lt;canvas id="canvas" width="400" height="200" class="playable-canvas"&gt;&lt;/canvas&gt;
&lt;div class="playable-buttons"&gt;
  &lt;input id="edit" type="button" value="Edit" /&gt;
  &lt;input id="reset" type="button" value="Reset" /&gt;
&lt;/div&gt;
&lt;textarea id="code" class="playable-code"&gt;
ctx.beginPath();
ctx.moveTo(0,0);
ctx.lineTo(100, 100);
ctx.stroke();&lt;/textarea&gt;
</pre>

<pre class="brush: js">var canvas = document.getElementById("canvas");
var ctx = canvas.getContext("2d");
var textarea = document.getElementById("code");
var reset = document.getElementById("reset");
var edit = document.getElementById("edit");
var code = textarea.value;

function drawCanvas() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  eval(textarea.value);
}

reset.addEventListener("click", function() {
  textarea.value = code;
  drawCanvas();
});

edit.addEventListener("click", function() {
  textarea.focus();
})

textarea.addEventListener("input", drawCanvas);
window.addEventListener("load", drawCanvas);
</pre>
</div>

<p>{{ EmbedLiveSample('Playable_code', 700, 360) }}</p>

<h2 id="规范描述">规范描述</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.CanvasRenderingContext2D.lineTo")}}

<h2 id="参见">参见</h2>

<ul>
 <li>接口定义， {{domxref("CanvasRenderingContext2D")}}</li>
 <li>{{domxref("CanvasRenderingContext2D.moveTo()")}}</li>
 <li>{{domxref("CanvasRenderingContext2D.stroke()")}}</li>
</ul>