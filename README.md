# Glassmorphism Calculator
 Glassmorphism Calculator using Vanilla JavaScript
***
#### HTML
```html
<div class="container">
	<form class="calculator" name="calc">
		<input type="text" readonly class="value" name="txt">
		<span class="num clear" onclick="calc.txt.value=''">c</span>
		<span class="num" onclick="document.calc.txt.value +='/'">/</span>
		<span class="num" onclick="document.calc.txt.value +='*'">*</span>
		<span class="num" onclick="document.calc.txt.value +='7'">7</span>
		<span class="num" onclick="document.calc.txt.value +='8'">8</span>
		<span class="num" onclick="document.calc.txt.value +='9'">9</span>
		<span class="num" onclick="document.calc.txt.value +='-'">-</span>
		<span class="num" onclick="document.calc.txt.value +='4'">4</span>
		<span class="num" onclick="document.calc.txt.value +='5'">5</span>
		<span class="num" onclick="document.calc.txt.value +='6'">6</span>
		<span class="num plus" onclick="document.calc.txt.value +='+'">+</span>
		<span class="num" onclick="document.calc.txt.value +='1'">1</span>
		<span class="num" onclick="document.calc.txt.value +='2'">2</span>
		<span class="num" onclick="document.calc.txt.value +='3'">3</span>
		<span class="num" onclick="document.calc.txt.value +='0'">0</span>
		<span class="num" onclick="document.calc.txt.value +='00'">00</span>
		<span class="num" onclick="document.calc.txt.value +='.'">.</span>
		<span class="num equal" onclick="document.calc.txt.value =eval(calc.txt.value)">=</span>
	</form>
</div>
```
#### CSS
```css
*{ padding: 0; margin: 0; box-sizing: border-box; }
body{ display: flex; justify-content: center; align-items: center; min-height: 100vh; background-color: #091921; font-family: 'Quicksand', sans-serif;}
body::before{ content: ''; position: absolute; left: 0; top: 0; width: 100%; height: 100%; background: linear-gradient(#e91e63, #ffc107); clip-path: circle(22% at 30% 20%); }
body::after{ content: ''; position: absolute; left: 0; top: 0; width: 100%; height: 100%; background: linear-gradient(#ffffff, #da00ff); clip-path: circle(20% at 70% 90%); }
.container{ 
	position: relative;
	background: rgba(255,255,255,0.05);
	border-radius: 6px;
	overflow: hidden;
	z-index: 10;
	border-top: 1px solid rgba(255,255,255,0.2);
	border-left: 1px solid rgba(255,255,255,0.2);
	box-shadow: 5px 5px 30px rgba(0,0,0,.2);
	backdrop-filter: blur(15px);
}
.calculator{
	position: relative;
	display: grid;
}
.calculator .value{
	grid-column: span 4;
	height: 140px;
	width: 300px;
	text-align: right;
	border: none;
	outline: none;
	padding: 10px;
	font-size: 30px;
	background: transparent;
	color: #fff;
	border-bottom: 1px solid rgba(255,255,255,0.05);
	border-right: 1px solid rgba(255,255,255,0.205);
}
.calculator span{
	display: grid;
	place-items: center;
	height: 75px;
	width: 75px;
	color: #fff;
	font-weight: 400;
	cursor: pointer;
	user-select: none;
	border-bottom: 1px solid rgba(255,255,255,0.05);
	border-right: 1px solid rgba(255,255,255,0.205);
	transition: 0.5s;
}
.calculator span:hover{
	transition: 0s;
	background-color: rgba(255,255,255,.05);
}
.calculator span:active{
	background: #14ff47;
	color: #192f00;
	font-size: 24px;
	font-weight: 500;
}
.calculator .clear{
	grid-column: span 2;
	width: 150px;
	background-color: rgba(255,255,255,0.05);
}
.calculator .plus{
	grid-row: span 2;
	height: 150px;
}
.calculator .equal{
	background-color: rgba(255,255,255,0.05);
}
```
#### JAVASCRIPT
```javascript
<script src="vanilla-tilt.js"></script>
<script>
	VanillaTilt.init(document.querySelector(".container"), {
		max: 15,
		speed: 400,
		glare: true,
		"max-glare": 0.2,
	});
</script>
```
