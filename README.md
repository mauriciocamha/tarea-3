# tarea-3
/index.html

<!DOCTYPE html>
<html>
<head>
 <! — incluir bootstrap y jquery cdn →
</head>
<body>
<div class=”container”>
 <br>
 <div class=”jumbotron”>
 <h1 class=”display-4">Enviar mensaje</h1>
 <br>
 <input id = “nombre” class=”form-control” placeholder=”Nombre”>
 <br>
 <textarea id = “mensaje” class=”form-control” placeholder=”Su mensaje aquí”>
</textarea>
 <br>
 <button id=”enviar” class=”btn btn-success”>Enviar</button>
 </div>
 <div id=”mensajes”>
 
</div>
</div>
<script>

</script>
</body>
</html>

app.use(express.static(__dirname));

npm install -g nodemon

nodemon ./server.js

npm install -s mongoose

var mongoose = require(‘mongoose’);

mongoose.connect(dbUrl , (err) => { 
   console.log(‘Mongodb conectado’,err);
})

ar Mensaje = mongoose.model(‘Mensaje’,{ nombre : String, mensaje: String})

var bodyParser = require(‘body-parser’)
app.use(bodyParser.json());
app.use(bodyParser.urlencoded({extended: false}))

app.get('/mensajes', (req, res) => {
  Mensaje.find({},(err, mensajes)=> {
    res.send(mensajes);
  })
})
