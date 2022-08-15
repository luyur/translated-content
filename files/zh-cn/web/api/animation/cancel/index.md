---
title: Animation.cancel()
slug: Web/API/Animation/cancel
---
<p>{{ SeeCompatTable() }}{{ APIRef("Web Animations") }}</p>

<p>{{domxref("Animation")}} 接口的 Web 动画 API 的 <code><strong>cancel()</strong></code> 方法将清除此动画造成的所有 {{domxref("KeyframeEffect")}}，并中止其播放。</p>

<div class="note">
<p>当一个动画被取消时，其 {{domxref("Animation.startTime", "startTime")}} 和 {{domxref("Animation.currentTime", "currentTime")}} 被设置为 null。</p>
</div>

<h2 id="语法">语法</h2>

<pre class="syntaxbox"><em>Animation</em>.cancel();</pre>

<h3 id="参数">参数</h3>

<p>无。</p>

<h3 id="返回值">返回值</h3>

<p>无。</p>

<h3 id="异常">异常</h3>

<p>这个方法不会直接抛出异常; 但是，如果动画的 {{domxref("Animation.playState", "playState")}} 取消时是除了“空闲”之外的任何东西，{{domxref("Animation.finished", "current finished promise", "", 1)}} 被拒绝与一个 {{domxref("DOMException")}} 命名的<code>AbortError</code>.</p>

<dl>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容">浏览器兼容</h2>

{{Compat("api.Animation.cancel")}}

<h2 id="相关内容">相关内容</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Web_Animations_API">Web Animations API</a></li>
 <li>{{domxref("KeyframeEffect")}}</li>
 <li>{{domxref("Animation")}}</li>
 <li>{{domxref("Animation.playState")}}</li>
 <li>{{domxref("Animation.finished")}} returns the promise this action will reject if the animation's <code>playState</code> is not <code>"idle"</code>.</li>
</ul>