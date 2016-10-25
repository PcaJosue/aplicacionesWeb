# aplicacionesWeb
<html ng-app="miapp">
	<head>
		<meta charset="utf-8">
		<script src="angular-1.5.8/angular.min.js">
		</script>
	</head>
	<body ng-app='control1'>
		{{"hola"}}
		<br>
		¿QUE OPINA SOBRE EL TRANSPORTE PUBLICO?
		<br>
		<pregunta name='a'></pregunta>
		<br>
		¿QUE OPINA SOBRE LOS PARQUES Y JARDINES?
		<br>
		<pregunta name='b'></pregunta>
		
		
		<script>
		var miapp=angular.module('miapp',[])
		.controller('control1',function(){})
		.directive('pregunta',function(){
				var obj={
					restrcict:'E',
					link: function(scope,elemento,atributo)
					{
						elemento.html("<input type='range' id='"+
						atributo.name+"' min='1' max='5'> " +
						"<img id='"+atributo.name+"c' src='imagenes/3.gif'>"
						+ "<audio id='"+atributo.name+"b' src='sonidos/s3.mp3' autoplay preload='auto'></audio>");
						elemento.on('change',function()
						{
							var p=document.getElementById(atributo.name);
							var pc=document.getElementById(atributo.name+'c');
							var pb=document.getElementById(atributo.name+'b')
							pc.src='imagenes/'+p.value+'.gif';
							pb.src='sonidos/s'+p.value + '.mp3';
						});
					}
				}
				return obj;
		}
	
	)
</script>
</body>
</html>
