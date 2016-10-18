# aplicacionesWeb
<html ng-app="miapp">
	<script src="E:/AplicacioneWeb/angular-1.5.8/angular.js"> </script>
		<body ng-controller='control1'>
		{{titulo}}
		<reloj modo='fecha'/ estilo="gallina">
		<script>
		var miapp=angular.module('miapp',[])
		.controller('control1',function($scope)
								{
								$scope.titulo='Mi aplicacion';
								}
					).directive('reloj', function($interval){
					var obj;
				obj=
				{restrict:'E',link:function(scope,elemento,atributo)
					{
						if(atributo.estilo=='gallina'){
							elemento.css({background:'#ffffcc',font:'18px Arial'});
											
						};			
						function imprimirHora()
						{
							var fh=new Date();
							if(atributo.modo=='hora')
							{
								elemento.html(fh.toLocaleTimeString());
							}
							else if (atributo.modo=='fecha')
							{
								elemento.html(fh.toLocaleString());
							}
						}
					mireloj=$interval(imprimirHora,1000);
					}
				};
			return obj;
			});
		</script>
	</body>
</html>
