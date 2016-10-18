# aplicacionesWeb

<html ng-app="miapp">
	<script src="E:/AplicacioneWeb/angular-1.5.8/angular.js"> </script>
		<body ng-controller='control1'>
		{{titulo}}
		<reloj modo='hora'/>
		<script>
		var miapp=angular.module('miapp',[])
		.controller('control1',function($scope)
								{
								$scope.titulo='Mi aplicacion';
								
								}
					).directive('reloj', function($interval){
					var objeto;
					obj={restrict:'E',template:'mi reloj'};
					return obj
					});

					
					
		</script>
		</body>
</html>
