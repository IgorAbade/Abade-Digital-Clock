<!DOCTYPE html>
  <html lang="pt-BR">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-AU-Compatible" content="IE-edge">
    <meta name="viewport" content="width=device-width", initial-scale=1.0>
    
     <link rel="stylesheer" href="style.css">
    </head>
    <body>
   <div class="relogio">   
    <div>    
      <span id="horas">00</span>
      <span class="tempo">Horas</span>
    </div>
    <div>
       <span id="minutos">00</span>
      <span class="tempo">minutos</span>
    </div>
    <div>
       <span id="segundos">00</span>
      <span class="tempo">segundos</span>
    </div>
    </div>
    <script src="index.js"></script>
  </body>
  </html>
    
    *{
  padding: 0;
  margin: 0;
  font-family: "Andale Mono", AndaleMono, monospace;
  color: #50fe00;
}

body{
  height: 100vh;
  background: linear-gradient(0deg, rgba(2,3,5,1) 0%, rgba(80,254,0,1) 100%);
  display: flex;
  align-items: center;
  justify-content: center;
}

.relogio{
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 200px;
  width: 550px;
  background: black;
  border-style: double;
  box-shadow: 0px 0px 8px 10px;
  
}

.relogio div{
  height: 170px;
  width: 150x;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: 60px;
}

.relogio span{
  font-weight: lighter;
  font-size: 60px;
}

.relogio span.tempo{
  font-size: 20px;
}

const horas = document.getElementById('horas');
const minutos = document.getElementById('minutos');
const segundos = document.getElementById('segundos');

const relogio = setInterval(function time() {
    let dateToday = new Date();
    let hr = dateToday.getHours();
    let min = dateToday.getMinutes();
    let s = dateToday.getSeconds();

    if (hr < 10) hr = '0' + hr;

    if (min < 10) min = '0' + min;

    if (s < 10) s = '0' + s;

    horas.textContent = hr;
    minutos.textContent = min;
    segundos.textContent = s;

})
