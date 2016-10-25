# aplicacionesWeb
<html ng-app="miapp">
	<head>
		<meta charset="utf-8">
		<script src="angular-1.5.8/angular.min.js">
		</script>
	</head>
	<body ng-app='control1'>
		{{"hola"}}
		<pregunta name='a'></pregunta>
		<pregunta name='b'></pregunta>
		
		
		<script>
		var miapp=angular.module('miapp',[])
		.controller('control1',function(){})
		.directive('pregunta',function(){
				var obj={
					restrcict:'E',
					link: function(scope,elemento,atributo)
					{
						elemento.html("<input type='range' id='"+atributo.name+"' min='1' max='5'><div id='"+atributo.name+"c'></div>");
						elemento.on('change',function()
						{
							var p=document.getElementById(atributo.name);
							var pc=document.getElementById(atributo.name+'c');
							pc.innerHTML=p.value;
						});
					}
				}
				return obj;
		}
	
	)
</script>
</body>
</html>
