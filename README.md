cursorWatcher
=============

Nesneye göre farenin 9 farklı konumunu yakalayıp işlem yapmanızı sağlar.

[Daha somut Örnekler için tıklayın](http://www.erbilen.net/lab/cursorWatcher/)

Nesneye göre konumlar:
- Yukarı
- Aşağı
- Sol
- Sağ
- Yukarı Sol
- Yukarı Sağ
- Aşağı Sol
- Aşağı Sağ
- Orta

HTML Yapısı
=============

```html
<div class="test">
	<div></div>
</div>
```

CSS
=============

```css
.test {
	width: 300px;
	height: 300px;
	background: rgba(255,255,255,.2);
	position: absolute;
	top: 50%;
	left: 50%;
	margin-top: -150px;
	margin-left: -150px;
}
.test div {
	height: 100%;
}
```

Kullanımı
=============

```javascript
var body = $('body');
$('.test div').cursorWatcher({
	center: function () {
		body.css('background-color','#95a5a6');
	},
	top: function () {
		body.css('background-color','#1abc9c');
	},
	topLeft: function () {
		body.css('background-color','#2ecc71');
	},
	topRight: function () {
		body.css('background-color','#3498db');
	},
	right: function () {
		body.css('background-color','#9b59b6');
	},
	left: function () {
		body.css('background-color','#34495e');
	},
	bottom: function () {
		body.css('background-color','#f1c40f');
	},
	bottomLeft: function () {
		body.css('background-color','#e67e22');
	},
	bottomRight: function () {
		body.css('background-color','#e74c3c');
	}
});
```
