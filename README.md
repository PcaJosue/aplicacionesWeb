<html ng-app="miapp">
	<head>
		<meta charset="utf-8">
		<link href="E:\WEB\bootstrap-3.3.7-dist\css\bootstrap.min.css" rel="stylesheet">
		<script src="E:\WEB\bootstrap-3.3.7-dist\js\bootstrap.min.js"></script>
		<script src="E:\WEB\angular-1.5.8/angular.js">
		</script>
	</head>
	<body ng-controller='control1'>
		<div class= "btn-group">
		<div style="background-color: #0072bc; width:200px ; height:200px">
		<pregunta1> </pregunta1>
		<pregunta1> </pregunta1>
		</div>
		<button type="button" class="btn btn-default dropdown-toogle" data-toogle="dato" aria-haspopup="true" aria-expanded="false">
		{{"Action"}} <span class="caret"> </span>
		</button>
		</div>
		<script>
		var miapp=angular.module('miapp',[])
		.controller('control1',function($scope){})
		.directive('pregunta1',function(){
			var obj={
			restrict: 'E',
			link: function(scope,elemento,atributo){
			var estado=1;
            elemento.html('<img src="cat/cat_a'+estado+'.gif"/>');
            elemento.on('click',function(){
                    estado++;
                    estado= estado==10 ? 1:estado;
                     elemento.html('<img src="cat/cat_a'+estado+'.gif"/>');
                });
			}
			};
			return obj;
			})
		;
		</script>
</body>
</html>
