# aplicacionesWeb
<html ng-app="miapp">
<head>
<meta charset="UTF-8">
<script src="D:/web/angular-1.5.8/angular.min.js"></script>
<style>
.iconoEvaluacion{width:50px}
</style>
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
		<label for="pesimo"><img src="D:/web/imagenes/pesimo.jpg" class="iconoEvaluacion"></label>
		<input type='radio' name="transpublic" id="pesimo">
		</td>
		
		<td>
		<label for="malo"><img src="D:/web/imagenes/malo.jpg" class="iconoEvaluacion"></label>
		<input type='radio' name="transpublic" id="malo">
		</td>
		
		<td>
		<label for="aceptable"><img src="D:/web/imagenes/aceptable.jpg" class="iconoEvaluacion"></label>
		<input type='radio' name="transpublic" id="aceptable">
		</td>
		
		<td>
		<label for="bueno"><img src="D:/web/imagenes/bueno.jpg" class="iconoEvaluacion"></label>
		<input type='radio' name="transpublic" id="bueno">
		</td>
		
		<td>
		<label for="excelente"><img src="D:/web/imagenes/excelente.jpg" class="iconoEvaluacion"></label>
		<input type='radio' name="transpublic" id="excelente">
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
