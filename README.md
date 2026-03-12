# Calculator-
<!DOCTYPE html>
<html>
<head>
<title>Calculator</title>

<style>

body{
font-family: Arial;
background:#dfe6e9;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
}

.calculator{
background:#2d3436;
padding:20px;
border-radius:10px;
}

#display{
width:100%;
height:60px;
font-size:28px;
text-align:right;
margin-bottom:10px;
padding:10px;
border:none;
}

button{
width:60px;
height:60px;
margin:5px;
font-size:22px;
border:none;
border-radius:8px;
cursor:pointer;
}

.number{
background:#ecf0f1;
}

.operator{
background:#74b9ff;
color:white;
}

.equal{
background:#e17055;
color:white;
width:130px;
}

.clear{
background:#d63031;
color:white;
}

</style>
</head>

<body>

<div class="calculator">

<input type="text" id="display" disabled>

<br>

<button class="clear" onclick="clearDisplay()">C</button>
<button onclick="append('%')">%</button>
<button onclick="append('/')">÷</button>
<button class="operator" onclick="append('*')">×</button>

<br>

<button class="number" onclick="append('7')">7</button>
<button class="number" onclick="append('8')">8</button>
<button class="number" onclick="append('9')">9</button>
<button class="operator" onclick="append('-')">-</button>

<br>

<button class="number" onclick="append('4')">4</button>
<button class="number" onclick="append('5')">5</button>
<button class="number" onclick="append('6')">6</button>
<button class="operator" onclick="append('+')">+</button>

<br>

<button class="number" onclick="append('1')">1</button>
<button class="number" onclick="append('2')">2</button>
<button class="number" onclick="append('3')">3</button>

<br>

<button class="number" onclick="append('0')">0</button>
<button onclick="append('.')">.</button>
<button class="equal" onclick="calculate()">=</button>

</div>

<script>

function append(value){
document.getElementById("display").value += value;
}

function clearDisplay(){
document.getElementById("display").value = "";
}

function calculate(){
try{
document.getElementById("display").value = eval(document.getElementById("display").value);
}
catch{
alert("Invalid");
}
}

</script>

</body>
</html>
