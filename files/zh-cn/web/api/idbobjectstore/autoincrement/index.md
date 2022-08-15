---
title: IDBObjectStore.autoIncrement
slug: Web/API/IDBObjectStore/autoIncrement
---
<p>{{ APIRef("IndexedDB") }}</p>

<div>
<p>{{domxref("IDBObjectStore")}}的只读属性<strong><code>autoIncrement</code></strong>接口返回当前 objectStore 的自增标记值（true 或 false）。</p>

<p>什么是自增呢？熟悉 SQL 的朋友应该知道，SQL 数据里面的字段可以设置自增，当一条记录被插入时，不必传入该字段，新记录的该字段值会在前面一条记录该字段值的基础上加 1.而 indexedDB 里面的 autoIncrement 的同样的意义。（译者注）</p>

<p>注意：每个 objectStore 的 auto increment 计数器是分开独立的。</p>

<p>{{AvailableInWorkers}}</p>
</div>

<h2 id="句法">句法</h2>

<pre class="syntaxbox">var <em>myAutoIncrement</em> = <em>objectStore</em>.autoIncrement;</pre>

<h3 id="Value">Value</h3>

<p>{{domxref("Boolean")}}:</p>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">值</th>
   <th scope="col">含义</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>true</code></td>
   <td>当前 objectStore 会自增</td>
  </tr>
  <tr>
   <td><code>false</code></td>
   <td>当前 objectStore 不会自增<br>
     </td>
  </tr>
 </tbody>
</table>

<h2 id="例子">例子</h2>

<p>在下面代码片段中，我们在数据库里打开了一个可读写的事务（transaction），并且用<code>add()</code>向一个 objectStore 中添加了一些数据。在 objectStore 被创建之后，我们在 console 中打印了 objectStore.autoIncrement 的值。想查看完整的例子，请查看我们的<a href="https://github.com/mdn/to-do-notifications/">To-do Notifications</a>应用（<a href="http://mdn.github.io/to-do-notifications/">查看在线例子</a>）。</p>

<pre class="brush: js" style="font-size: 14px;">// Let us open our database
var DBOpenRequest = window.indexedDB.open("toDoList", 4);

DBOpenRequest.onsuccess = function(event) {
  note.innerHTML += '&lt;li&gt;Database initialised.&lt;/li&gt;';

  // store the result of opening the database in the db variable.
  // This is used a lot below
  db = DBOpenRequest.result;

  // Run the addData() function to add the data to the database
  addData();
};

function addData() {
  // Create a new object ready to insert into the IDB
  var newItem = [ { taskTitle: "Walk dog", hours: 19, minutes: 30, day: 24, month: "December", year: 2013, notified: "no" } ];

  // open a read/write db transaction, ready for adding the data
  var transaction = db.transaction(["toDoList"], "readwrite");

  // report on the success of the transaction completing, when everything is done
  transaction.oncomplete = function(event) {
    note.innerHTML += '&lt;li&gt;Transaction completed.&lt;/li&gt;';
  };

  transaction.onerror = function(event) {
    note.innerHTML += '&lt;li&gt;Transaction not opened due to error. Duplicate items not allowed.&lt;/li&gt;';
  };

  // create an object store on the transaction
  var objectStore = transaction.objectStore("toDoList");
  console.log(objectStore.autoIncrement);

  // Make a request to add our newItem object to the object store
  var objectStoreRequest = objectStore.add(newItem[0]);

  objectStoreRequest.onsuccess = function(event) {
    // report the success of our request
    note.innerHTML += '&lt;li&gt;Request successful.&lt;/li&gt;';
  };
};</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="Browser_compatibility">浏览器兼容性</h2>

<div>
<p>{{Compat}}</p>
</div>

<h2 id="相关内容">相关内容</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/IndexedDB_API/Using_IndexedDB">使用 IndexedDB</a></li>
 <li>开始学习事务 transactions: {{domxref("IDBDatabase")}}</li>
 <li>使用事务 transactions: {{domxref("IDBTransaction")}}</li>
 <li>key 值域 range 的使用: {{domxref("IDBKeyRange")}}</li>
 <li>检索、修改: {{domxref("IDBObjectStore")}}</li>
 <li>使用游标: {{domxref("IDBCursor")}}</li>
 <li>相关例子：<a href="https://github.com/mdn/to-do-notifications/tree/gh-pages">To-do Notifications</a> (<a href="http://mdn.github.io/to-do-notifications/">view example live</a>.)</li>
</ul>