# aplicacionesWeb
<html ng-app="miapp">
<head>
<meta charset="UTF-8">
<script src="D:/web/angular-1.5.8/angular.min.js"></script>
<style>
.iconoEvaluacion{width:50px}
#parque{
width:150px;
}
#trole{
width:150px;
}
#calle{
width:150px;
}

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
		<tr> <td  class='pregunta'>
		<p> Que opina sobre <img src="imagenes/trole.jpg" id="trole" /> ? <evaluacion pregunta="1"/></p> 
		<p> Que opina sobre <img src="imagenes/parque.jpg" id="parque" /> ? <evaluacion pregunta="2"/></p>
		<p> Que opina sobre <img src="imagenes/calle.jpg" id="calle" /> ? <evaluacion pregunta="3"/></p> 
		</td></tr>		
		</td></tr>
		<tr>
		<td>
		
		
		
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
			elemento.html('<img src="imagenes/1.jpg" width=50 height=50/> ');
			elemento.on('click',function(){
			puntos++;
			if(puntos>5) puntos=1;
			elemento.html('<img src="imagenes/'+puntos+'.jpg" width=50 height=50/>');
			})
		}}
		return obj;
		});
		</script>
	</body>
</html>
