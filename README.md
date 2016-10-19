# aplicacionesWeb
<html ng-app="miapp">
<head>
<meta charset="UTF-8">
<script src="D:/web/angular-1.5.8/angular.min.js"></script>
<style>
.iconoEvaluacion{width:50px}
</style>
<script>
function mostrarIcono(){
var p=document.getElementById("puntos");
p.addEventListener('change',function(){
var valor=document.getElementById("puntos").value;
var cara=document.getElementById("cara").innerHTML=valor;
});

}

</script>
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
		
		<evaluacion/>
		
		
		</td>
		
		</tr>
		</table>
	</form>
		<script> 
		var mipp=angular.module('miapp',[])
		.controller('control1',function($scope){
		$scope.encuesta='Encuesta sobre servicios publicos';
		})
		.directive('evaluacion',function($interval){
		var puntos=1;
		var obj={
		restrict:'E',link:function(scope,elemento,atributo){
			elemento.html('<img src="imagenes/1.jpg"/>');
			elemento.on('click',function(){
			puntos++;
			if(puntos>5) puntos=1;
			elemento.html('<img src="imagenes/'+puntos+'.jpg"/>');
			})
		}}
		return obj;
		});
		</script>
	</body>
</html>
