<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Lector de Patentes</title>

<style>
body{
  margin:0;
  font-family:Arial;
  background:#012b63;
  color:white;
  display:flex;
  justify-content:center;
  align-items:center;
  height:100vh;
}

.card{
  width:90%;
  max-width:400px;
  background:rgba(255,255,255,0.08);
  padding:20px;
  border-radius:20px;
  text-align:center;
}

input{
  width:100%;
  padding:15px;
  border-radius:12px;
  border:none;
  font-size:18px;
  margin-top:10px;
}

button{
  width:100%;
  padding:15px;
  margin-top:15px;
  border:none;
  border-radius:12px;
  background:#0d6efd;
  color:white;
  font-weight:bold;
  cursor:pointer;
}

.status{
  margin-top:10px;
  font-size:14px;
  opacity:0.8;
}
</style>
</head>

<body>

<div class="card">

  <h2>🚘 Lector de Patentes</h2>

  <input id="patente" placeholder="Patente detectada">

  <button onclick="abrirCamara()">📸 ESCANEAR PATENTE</button>

  <input type="file" id="camara" accept="image/*" capture="environment" style="display:none"
         onchange="procesarImagen(event)">

  <div class="status" id="status">Esperando acción...</div>

</div>

<script>

const API_URL = "https://script.google.com/macros/s/AKfycbwp_bpFtVONamA-i4GtC51KNWYnic0FMYBCg_Vt6WGlYg8Cy8TrZqQFOC2ST_dbclW7/exec";

function abrirCamara(){
  document.getElementById("camara").click();
}

async function procesarImagen(event){
  const file = event.target.files[0];
  if(!file) return;

  document.getElementById("status").innerText = "Analizando imagen...";

  const reader = new FileReader();

  reader.onload = async function(){

    const base64 = reader.result.split(",")[1];

    try{
      const res = await fetch(API_URL, {
        method:"POST",
        body: JSON.stringify({ image: base64 })
      });

      const data = await res.json();

      console.log("RESPUESTA:", data);

      if(data.ok && data.patente){
        document.getElementById("patente").value = data.patente;
        document.getElementById("status").innerText = "Patente detectada ✔";
      } else {
        document.getElementById("status").innerText = "No se detectó patente";
      }

    } catch(e){
      console.error(e);
      document.getElementById("status").innerText = "Error de conexión";
    }
  };

  reader.readAsDataURL(file);
}

</script>

</body>
</html>
