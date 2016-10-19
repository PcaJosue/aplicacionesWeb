# aplicacionesWeb
<html ng-app="miapp">
<head>
<meta charset="UTF-8">
<script src="D:/web/angular-1.5.8/angular.min.js"></script>
</head>
	<body ng-controller='control1'>
	<h1>{{encuesta}}</h1>
	<form>
		
		<table class='cuestionario'>
		<tr> <td colspan='5' class='pregunta'>
		<p> Que opina sobre el transporte publico </p>
		</td></tr>
		<tr>
		<td>
		<label for="pesimo">Pesimo</label>
		<input type='radio' name="transpublic" id="pesimo">
		</td>
		
		<td>
		<label for="pesimo">Malo</label>
		<input type='radio' name="transpublic" id="pesimo">
		</td>
		
		<td>
		<label for="pesimo">Aceptable</label>
		<input type='radio' name="transpublic" id="pesimo">
		</td>
		
		<td>
		<label for="pesimo">Bueno</label>
		<input type='radio' name="transpublic" id="pesimo">
		</td>
		
		<td>
		<label for="pesimo">Excelente</label>
		<input type='radio' name="transpublic" id="pesimo">
		</td>
		
		</tr>
		</table>
	</form>
		<script> 
		var mipp=angular.module('miapp',[])
		.controller('control1',function($scope){
		$scope.encuesta='Encuesta sobre servicios publicos';
		}
		);
		</script>
	</body>
</html>
