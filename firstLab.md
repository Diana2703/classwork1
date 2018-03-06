<!DOCTYPE html>
<html>
	<head>
		<title>
			Лабораторная работа №1
		</title>
		<script>
			function getElem() 
			{
				var mA = document.getElementById("massA").value;
				var mB = document.getElementById("massB").value;
				if (mA != "")
				{
					document.getElementById("result").innerHTML = "Введён массив A = "+mA + "<br/>";
					mA = mA.split(" ");
					document.getElementById("result").innerHTML += "Массив A = "+mA + "<br/>";
					for (var i = 0; i < mA.length; i++)
						document.getElementById("result").innerHTML += "Элемент["+i+"] = "+mA[i] + "<br/> " ;
					document.getElementById("result").innerHTML += "<br/>";
				}
				if (mB != "")
				{
					document.getElementById("result").innerHTML += "Введён массив B = "+mB + "<br/>";
					mB = mB.split(" ");
					document.getElementById("result").innerHTML += "Массив B = "+mB + "<br/>";
					for (var i = 0; i < mB.length; i++)
						document.getElementById("result").innerHTML += "Элемент["+i+"] = "+mB[i] + "<br/>";
					document.getElementById("result").innerHTML += "<br/>";
				}
			}
			
			function ClearThis(el)
			{
				el.innerHTML = "";
			}
		</script>
	</head>
	<body>
		<form>
			Введите массив А
			<input type="text" name="array1" id = "massA"> <br>
			Введите массив B
			<input type="text" name="array2" id = "massB"> <br>
			<input type="button" onclick="getElem()" value="Send">
		</form>
		Вывод результата <br />
		<div id = "result" onClick = "ClearThis(this);"> </div>
	</body>
</html>
